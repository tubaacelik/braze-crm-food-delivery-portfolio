# FoodieGo CRM Lifecycle Automation with Braze

> Personal CRM portfolio project created in a Braze free-trial environment using demo and Kaggle-based data. The journeys were designed and validated as drafts; they were not launched to real customers.

## Project overview

This project demonstrates how raw food-delivery order data can be transformed into audience-ready CRM data and used to design lifecycle journeys in Braze.

Two use cases were developed:

1. **New User Welcome Journey** — activates users during their first week.
2. **Inactive Customer Win-Back Journey** — re-engages customers who have not used the app recently.

## Business problem

Food-delivery products need different communication for new and inactive customers. A single campaign for every user can create irrelevant messaging. This project separates those lifecycle stages and assigns each one a purpose-built journey.

## Data preparation

The source order dataset was prepared in Kaggle with Python and Pandas. The workflow included data-quality checks, user-level aggregation and export to a Braze-compatible CSV format.

## Segmentation

### New Users – First Week

Users whose first app use was less than one week ago.

### Inactive Customers – Win Back

Users whose last app use was before July 23, 2026. The segment contained **81 estimated users**, representing **8.1%** of the demo workspace.

![Created CRM segments](assets/01-created-segments.png)

## Journey 1: New User Welcome

- Immediate entry after launch
- Audience: `New Users–First week`
- Re-entry disabled
- Email subject: `FoodieGo’ya hoş geldin! İlk lezzetini keşfet 🍕`
- Conversion event: session start within three days

![Welcome Canvas setup](assets/02-welcome-canvas-overview.png)

![Welcome email step](assets/03-welcome-message-step.png)

## Journey 2: Customer Win-Back

- Audience: `Inactive Customers – Win Back`
- Initial “Seni özledik” email
- Three-day evaluation window
- `Returned to App` branch for users who start a session
- `Everyone Else` branch followed by a reminder email
- Returning users exit the Canvas

![Win-back audience rule](assets/04-winback-segment.png)

![Win-back Canvas flow](assets/05-winback-canvas-flow.png)

## Tools

- Braze Segments and Canvas
- Python and Pandas
- Kaggle Notebooks
- CSV data preparation
- Email lifecycle design

## What this project demonstrates

- Lifecycle-based audience segmentation
- Behaviour-driven customer journeys
- Conversion-event configuration
- Action Paths and fallback messaging
- Consent-aware email targeting
- Translating prepared data into a CRM use case

## Limitations

The project was built in a Braze free-trial workspace. Canvas launch was unavailable, so the user counts shown are target-audience estimates rather than campaign results. No claim is made about actual sends, revenue uplift or conversion performance.

## Portfolio links

- Kaggle notebook: to be added
- Medium case study: to be added
- Portfolio page: to be added

