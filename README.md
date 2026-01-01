# CALL_FLOW09_Premium_Customer_Call_Routing_Using_Genesys_Cloud_Salesforce_CRM

#  Premium Customer Call Routing – Genesys Cloud
# Project Overview
  
  This project demonstrates Premium Customer Call Routing using Genesys Cloud integrated with Salesforce CRM.
  The solution dynamically identifies premium customers and provides agents with an enhanced UI for better call handling.

 # Key Features

   Salesforce CRM integration
   Premium customer identification
   Dynamic agent UI scripting
   Customer banner display
   Real-time customer details (Name, Number, Premium Status)
   Improved agent efficiency

 # Technologies Used

    Genesys Cloud CX
    
    Genesys Architect
    
    Genesys Scripting
    
    Salesforce CRM
    
    REST API
    
    JSON
    
    Call Flow Design

#  Call Flow Logic

  Incoming call received
  
  Caller number sent to Salesforce
  
  Salesforce returns:
  
  Customer Name
  
  Phone Number
  
  Premium Status
  
  Genesys Script updates agent UI:
  
  Top banner shows Premium status
  
  Right panel shows customer details
  
  Call routed based on customer type
  
#  Agent UI Behavior

   Banner displayed for Premium Customers
   Customer Name & Number shown
   Premium status highlighted
   Faster call handling
   
#  Architecture Diagram

  Caller → Genesys Cloud → Salesforce API
        ↓
   Agent UI (Scripted View)


# Success Response (Sample) 

{
  "searchRecords": [
    {
      "attributes": {
        "type": "Contact"
      },
      "Name": "Anubhav Rajput",
      "Phone": "+919876543210",
      "Premium_Customer__c": true
    }
  ]
}


# Success Template (Genesys)

{
  "customerName": "${searchRecords[0].Name}",
  "phoneNumber": "${searchRecords[0].Phone}",
  "premiumCustomer": ${searchRecords[0].Premium_Customer__c}
}


# Failure Response Handling

Failure Conditions

Customer not found

API timeout

Authentication failure

# Failure Output

{
  "customerName": "Unknown",
  "premiumCustomer": false
}

#  Usage in Architect Flow
# Step-by-Step:

    Collect ANI
    
    Use Call.Ani
    
    Invoke Data Action
    
    Action Name: Get_Customer_Details
    
    Input: phoneNumber = Call.Ani
    
    Decision Block
    
    If premiumCustomer = true
    → Route to Premium Queue
    
    Else
    → Normal Call Flow
    
    Agent Script Display
    
    Show:
    
    Customer Name
    
    Phone Number
    
    Premium Status Banner
