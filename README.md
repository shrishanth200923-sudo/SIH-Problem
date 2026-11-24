# SIH-Problem
Problem Statement:
Multiple intermediaries reduce farmers’ earnings and increase consumer prices.

Problem Description:
In India, produce passes through many hands (commission agents, wholesalers, transporters, retailers) before it reaches the consumer. Farmers often receive only 25-40% of the final consumer price. Consumers pay more, and farmers have no price transparency or bargaining power. Delayed payments and post-harvest losses make it worse.

Proposed Solution:
KisanDirect is a mobile and web platform that connects farmers and FPOs directly with consumers, retailers and restaurants. It has:👇

Easy listing:
o The farmer lists produce (type, quantity, quality, location) by app, SMS or voice in a regional language.
o AI fair-price engine: It predicts a fair price using mandi data (Agmarknet/eNAM), weather and demand trends, so farmers are not underpaid.
o Smart matching: Orders are matched to the nearest buyers to reduce transport cost and spoilage.
o Secure direct payment: Buyers pay by UPI into escrow. Money is released to the farmer’s bank account on delivery, so there are no payment delays.
o Shared logistics: Pickups from nearby farmers are combined into one route, which lowers delivery cost.
o Traceability: A QR code lets the buyer see the farm, harvest date and price breakup
Technical Approach:

<img width="1657" height="953" alt="image" src="https://github.com/user-attachments/assets/bcb2133f-31dd-4943-8c77-56a1d6cb1413" />
   o Frontend: React Native app (Android) and a React web portal, with multilingual and voice support.
   o Backend: Node.js/Python (FastAPI) microservices behind an API gateway, with OTP authentication.
   o Database: PostgreSQL for orders and users, Redis for caching.
   o AI/ML: A regression model (XGBoost/LSTM) for price prediction, using open mandi price and weather APIs.
   o Matching and routing: Geolocation-based matching using Google Maps/OpenStreetMap and a route-optimisation algorithm.
   o Payments: UPI/Razorpay escrow.
   o Traceability: Blockchain-based (or hash-chained) records, accessed through a QR code.
   o Deployment: Cloud (AWS/Azure) with Docker.
Impact:
   o Farmer income rises by an estimated 20-40%.
   o Consumer prices fall by an estimated 10-20%.
   o Post-harvest losses are lower because of faster sale and shorter supply chains.
   o Transparent pricing and faster payments help farmers financially.
Feasibility and Scalability:
 It starts with one district as a pilot, working with local FPOs. It then scales to other states using existing digital           infrastructure (UPI, eNAM, smartphones). The revenue model is a small 2-3% service fee, far below the commission  middlemen take.
