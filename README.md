# SIH-Problem

# SIH-Problem

**Name:** Shrishanth S

**Department:** AIML

**Year:** 1st Year

---
---

## Problem Statement:
Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Description:
In India, produce passes through many hands (commission agents, wholesalers, transporters, retailers) before it reaches the consumer. Farmers often receive only 25-40% of the final consumer price. Consumers pay more, and farmers have no price transparency or bargaining power. Delayed payments and post-harvest losses make it worse.

## Proposed Solution:
KisanDirect is a mobile and web platform that connects farmers and FPOs directly with consumers, retailers and restaurants. It has:

**Easy listing:**
- The farmer lists produce (type, quantity, quality, location) by app, SMS or voice in a regional language.
- **AI fair-price engine:** It predicts a fair price using mandi data (Agmarknet/eNAM), weather and demand trends, so farmers are not underpaid.
- **Smart matching:** Orders are matched to the nearest buyers to reduce transport cost and spoilage.
- **Secure direct payment:** Buyers pay by UPI into escrow. Money is released to the farmer's bank account on delivery, so there are no payment delays.
- **Shared logistics:** Pickups from nearby farmers are combined into one route, which lowers delivery cost.
- **Traceability:** A QR code lets the buyer see the farm, harvest date and price breakup.

## Technical Approach:

<img width="1657" height="953" alt="image" src="https://github.com/user-attachments/assets/bcb2133f-31dd-4943-8c77-56a1d6cb1413" />

- **Frontend:** React Native app (Android) and a React web portal, with multilingual and voice support.
- **Backend:** Node.js/Python (FastAPI) microservices behind an API gateway, with OTP authentication.
- **Database:** PostgreSQL for orders and users, Redis for caching.
- **AI/ML:** A regression model (XGBoost/LSTM) for price prediction, using open mandi price and weather APIs.
- **Matching and routing:** Geolocation-based matching using Google Maps/OpenStreetMap and a route-optimisation algorithm.
- **Payments:** UPI/Razorpay escrow.
- **Traceability:** Blockchain-based (or hash-chained) records, accessed through a QR code.
- **Deployment:** Cloud (AWS/Azure) with Docker.

## Impact:
- Farmer income rises by an estimated 20-40%.
- Consumer prices fall by an estimated 10-20%.
- Post-harvest losses are lower because of faster sale and shorter supply chains.
- Transparent pricing and faster payments help farmers financially.

## Feasibility and Scalability:
It starts with one district as a pilot, working with local FPOs. It then scales to other states using existing digital infrastructure (UPI, eNAM, smartphones). The revenue model is a sma:
ll 2-3% service fee, far below the commission middlemen take.


##Research and References:
   1. **Farmers' share of consumer price:** [RBI Bulletin: Mark-ups by intermediaries in agricultural markets](https://www.rbi.org.in/scripts/bs_viewbulletin.aspx?id=18527)
2. **Post-harvest losses:** [Lok Sabha Q.1872: Spoilage of fruits and vegetables](https://eparlib.nic.in/bitstream/123456789/2501891/1/AU1872.pdf)
3. **Mandi price data (AI fair-price engine):** [Agmarknet](https://agmarknet.gov.in/)
4. **eNAM (National Agriculture Market):** [eNAM Portal](https://enam.gov.in/web/)
5. **FPOs (Farmer Producer Organisations):** [PIB Factsheet: 10,000 FPOs Scheme](https://pib.gov.in/FactsheetDetails.aspx?Id=148588)
6. **Secure payments:** [Razorpay Route Documentation](https://razorpay.com/docs/payments/route/)
7. **Price prediction model:** [XGBoost Documentation](https://xgboost.readthedocs.io)
8. **Weather data:** [Open-Meteo](https://open-meteo.com)
9. **Maps and routing:** [OpenStreetMap](https://www.openstreetmap.org)

---

