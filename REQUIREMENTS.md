# Grocery Deal Tracker — Requirements Backlog

## 1. Project Overview

Grocery Deal Tracker is an application designed to help users save money on grocery shopping by monitoring prices and notifying users when products they are interested in go on sale.

The application's primary feature is a customizable watchlist where users can track frequently purchased groceries or products they plan to buy. Future functionality may include price history analysis, sale predictions, purchase urgency, and store distance preferences.

## 2. Requirements Backlog

**Priority Levels:**
- **Must Have:** Essential for the minimum viable product (MVP).
- **Should Have:** Important functionality but not essential for initial release.
- **Could Have:** Optional features for future development.

### Functional Requirements

| ID 		| Requirement / User Story 																																																						| Priority 		| Dependencies 													|
|---|---|---|---|
| FR-01 | As a user, I want to create an account and log in so that my preferences and watchlist are saved. 																	| Must Have 	| None 																	|
| FR-02 | As a user, I want to search for grocery products so that I can find items to track. 																								| Must Have 	| Product catalog/data source 					|
| FR-03 | As a user, I want to add and remove grocery products from my watchlist so that I can monitor products I am interested in. 					| Must Have 	| FR-01, FR-02 													|
| FR-04 | As a user, I want the application to track grocery prices and identify sales so that I can find discounted products. 								| Must Have 	| FR-02, price data source 							|
| FR-05 | As a user, I want to receive notifications when watchlisted products go on sale so that I can purchase them at discounted prices. 	| Must Have 	| FR-03, FR-04 													|
| FR-06 | As a user, I want to view current prices and discounts for watchlisted products so that I can compare deals. 												| Must Have 	| FR-03, FR-04 													|
| FR-07 | As a user, I want to select preferred grocery stores so that I only receive deals from stores I shop at. 														| Should Have | FR-01, store data 										|
| FR-08 | As a user, I want to specify a maximum distance for grocery stores so that I only receive notifications about nearby deals. 				| Should Have | FR-07, location data 									|
| FR-09 | As a user, I want to specify when I need to purchase an item so that the app can prioritize deals based on urgency. 								| Should Have | FR-03 																|
| FR-10 | As a user, I want to view historical prices for products so that I can determine whether a sale is worthwhile. 											| Should Have | FR-04, stored price history 					|
| FR-11 | As a user, I want the app to predict future sales based on historical price trends so that I can decide whether to buy now or wait. | Could Have 	| FR-10 																|
| FR-12 | As a user, I want to customize notification settings so that I can control which deals trigger alerts. 															| Should Have | FR-05 																|
| FR-13 | As a user, I want to compare prices for the same product across multiple stores so that I can identify the cheapest option. 				| Should Have | FR-04, FR-07 													|
| FR-14 | As a user, I want to track products from non-grocery retailers so that I can save money on other purchases. 												| Could Have 	| FR-02, FR-04, additional data sources |

### Non-Functional Requirements

| ID 		 | Requirement 																																																										| Priority 		| Category 				|
|---|---|---|---|
| NFR-01 | The application should display search results and watchlists within 3 seconds under normal operating conditions. 							| Should Have | Performance 		|
| NFR-02 | User account information and passwords must be stored securely, using industry-standard password hashing. 											| Must Have 	| Security 				|
| NFR-03 | The application should provide an intuitive interface that works on both desktop and mobile browsers. 													| Must Have 	| Usability 			|
| NFR-04 | The application should handle an increasing number of users and tracked products without significant performance degradation. 	| Should Have | Scalability 		|
| NFR-05 | Product prices should be updated at least once every 24 hours when the data provider supports that frequency. 									| Should Have | Data Freshness 	|

## 3. Initial Acceptance Criteria

**FR-03 — Product Watchlist**
- Users can add products from search results to their watchlist.
- Users can remove products from their watchlist.
- Watchlist contents persist after logging out and logging back in.

**FR-04 — Price Tracking**
- The system retrieves prices from an available retailer or pricing data source.
- The system stores the latest known price of tracked products.
- The system identifies a discount when the current price meets a defined sale criterion.

**FR-05 — Sale Notifications**
- Users can receive an alert when a watchlisted product meets the defined sale criterion.
- Notifications identify the product, store, and discounted price.
- Users do not receive duplicate notifications for the same unchanged deal.

**FR-08 — Store Distance Preferences**
- Users can specify a maximum store distance.
- Deals outside the selected distance are excluded from relevant alerts.
- Users can modify their distance preference.

**FR-11 — Sale Prediction**
- The system analyzes available historical pricing data.
- The system estimates when a product may go on sale again.
- Predictions are clearly labeled as estimates rather than guaranteed discounts.

## 4. MVP Scope

The minimum viable product will focus on the application's original purpose: allowing users to track products and receive notifications when they go on sale.

The proposed MVP includes FR-01 through FR-06, along with NFR-02 and NFR-03.

Advanced features such as sale predictions, purchase urgency, and non-grocery products will be considered for future iterations.

## 5. Assumptions and Open Questions

The following questions would require additional stakeholder input or research:

1. Which grocery stores will be supported initially?
2. Will pricing information come from retailer APIs, third-party providers, or another source?
3. What qualifies as a sale: an advertised discount, a price reduction, or a user-defined target price?
4. Will notifications be delivered through email, push notifications, or both?
5. How will the system handle unavailable or outdated product prices?

These questions should be resolved during subsequent requirements elicitation and refinement.
