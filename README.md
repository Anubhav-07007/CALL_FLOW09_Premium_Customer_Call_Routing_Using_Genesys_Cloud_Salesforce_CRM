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


screenshots/	Agent UI screenshots
🔹 Use Case

✔ Premium customer identification
✔ Priority handling
✔ Better agent experience
✔ CRM-based routing
