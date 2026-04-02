# AstraKarma — Apple Privacy Nutrition Label

---

## Does your app collect data?

**Yes**

---

## Data Types Collected

### 1. Contact Info

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Name | Yes | App Functionality, Product Personalization | Yes | No |
| Email Address | Yes | App Functionality, Authentication | Yes | No |
| Phone Number | No | — | — | — |
| Physical Address | No | — | — | — |

### 2. Health & Fitness

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Health | No | — | — | — |
| Fitness | No | — | — | — |

### 3. Location

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Precise Location | No | — | — | — |
| Coarse Location | Yes (birth city only) | App Functionality | Yes | No |

**Note:** The app collects the user's birth city (not current location) to calculate natal chart house positions. This is a one-time input during onboarding, not continuous tracking.

### 4. Sensitive Info

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Sensitive Info | No | — | — | — |

### 5. User Content

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Other User Content | Yes (birth date/time, gender, relationship status, daily Energy/Focus/Mood inputs) | App Functionality, Product Personalization | Yes | No |

### 6. Browsing History

Not collected.

### 7. Search History

Not collected.

### 8. Identifiers

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| User ID | Yes | App Functionality | Yes | No |
| Device ID | No | — | — | — |

### 9. Purchases

Not collected.

### 10. Usage Data

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Product Interaction | Yes | Analytics, App Functionality | Yes | No |

### 11. Diagnostics

| Data Type | Collected? | Purpose | Linked to Identity? | Tracking? |
|-----------|-----------|---------|---------------------|-----------|
| Crash Data | No dedicated crash diagnostics SDK in v1.0 | — | — | — |
| Performance Data | No | — | — | — |

---

## Summary for App Store Connect

When filling out the questionnaire, declare the following:

1. **Name** — App Functionality, Product Personalization — Linked to Identity — Not used for Tracking
2. **Email Address** — App Functionality — Linked to Identity — Not used for Tracking
3. **Coarse Location** — App Functionality — Linked to Identity — Not used for Tracking
4. **Other User Content** (birth data, pulse inputs) — App Functionality, Product Personalization — Linked to Identity — Not used for Tracking
5. **User ID** — App Functionality — Linked to Identity — Not used for Tracking
6. **Product Interaction** — Analytics — Linked to Identity — Not used for Tracking

Do not declare `Crash Data` unless a dedicated crash diagnostics SDK is added to the shipped app build later.

---

## Third-Party SDK Data Collection

Check each SDK in your project for their own data collection:

| SDK | Collects Data? | What? |
|-----|---------------|-------|
| Expo | No material collection in current shipped configuration | — |
| Supabase JS | Yes | Authentication identifiers and app data sent to your own Supabase instance |
| React Native Reanimated | No | Local animation library |
| expo-blur | No | Local UI component |
| expo-haptics | No | Local device API |
| expo-font | No | Local font loading |
| expo-localization | No | Reads device locale only |
| PostHog | Yes | Product interaction analytics and exception/error events |
| Anthropic API | Processes app data server-side | Birth chart context + pulse inputs sent by your backend to generate guidance |

**Important:** Anthropic API usage affects AI/transparency disclosures and privacy policy content, but it does not add a separate Apple privacy data category by itself beyond the user data already declared above. PostHog analytics is assumed to be enabled in the current production build and should be declared as `Product Interaction`; CTO should confirm the exact production configuration before submission. If you add ad networks, social SDKs, or dedicated crash reporting later, you must update this label before the next submission.

---

*Last updated: 2026-04-01*
