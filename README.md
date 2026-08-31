Vehicle Service Management Application

​This repository contains the documentation and architectural overview for the Vehicle Service Management application, developed on the Pega Platform™ for the 2026 Pega National Internship Program (NIP).  
​Project Overview

​Urban Fleet Operations provides vehicle servicing to individual customers across its service centres. Previously relying on emails and phone calls, this application digitizes and automates the end-to-end service workflow. The system enables customers to raise requests, allows service advisors to perform inspections and generate cost estimates, captures customer approvals, and automatically assigns work to technicians. 

​Key Features & User Stories
​The application is built around 10 core business requirements (User Stories):
​Service Initiation: Customers can submit a Vehicle Service Request capturing the Vehicle ID, Vehicle Model, and a description of the issue.  
​Inspection & Estimation: Service Advisors perform mandatory vehicle inspections, recording condition ratings and notes before generating a cost estimate.  
​Automated Cost Calculation: The system automatically aggregates Labor Cost and Parts Cost to derive the Total Cost using a declarative business rule.  
​Customer Approval Flow: Customers can review the itemized estimate and choose to approve or reject the service before execution begins.  
​Intelligent Routing: Approved requests are automatically routed to either the HeavyVehicleQueue or LightVehicleQueue based on the specified vehicle type.  
​Service-Level Agreements (SLA): Requests are tracked against a strict 2-day goal and a 3-day deadline to ensure timely resolution, with automated urgency escalations if deadlines are missed.  
​Automated Correspondence: Upon resolution, the system triggers a generated email notification summarizing the service details, vehicle information, and final cost for the customer.  

​Technical Architecture

​Case Lifecycle

​The Vehicle Service Request case type progresses through the following sequential stages:  
​Request Details: Initial intake of vehicle and issue data.  
​Inspection: Advisor assesses the vehicle and calculates costs.  
​Approval: Customer reviews and approves the total estimate.  
​Service Execution: Technicians fulfill the service request.  
​Resolution: Case closes and completion notifications are sent.

​Data Model

​Vehicle Data Object: A reusable entity created to maintain independent vehicle records, capturing properties such as Vehicle ID, Model, and Type to ensure data consistency across multiple service requests.  
​Access & Personas
​The application interface and routing are designed for three distinct personas:  
​Customer: Initiates requests, reviews estimates, and provides approvals.  
​Service Advisor: Conducts inspections and generates financial estimates.  
​Technician: Receives automated assignments and executes the physical vehicle service.  

​Development Details

​Platform: Pega Platform™ 8.x
​Initial Generation: Scaffolded using Pega Blueprint  
​Author: Aditya Kumar
