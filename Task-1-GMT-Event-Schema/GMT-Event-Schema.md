# Task 1 – GTM Event Schema

## GTM Event Tracking Plan

| Event Name | Trigger Type | Key Parameters (Minimum 3) | GA4 Report / Audience |
|------------|--------------|----------------------------|-----------------------|
| booking_step_complete | Custom Event (dataLayer) | step_number, step_name, clinic_location, specialty | Funnel Exploration |
| booking_completed | Custom Event | booking_id, clinic_location, specialty, appointment_date | Conversions Report |
| consultation_form_submitted | Form Submission | form_name, lead_source, city, phone_last4 | Conversions |
| call_now_clicked | Click Trigger | button_location, page_name, city | Engagement Report |
| whatsapp_clicked | Click Trigger | button_location, page_name, city | Engagement Report |
| patient_guide_downloaded | Link Click | guide_name, download_type, lead_source | Events Report |
| clinic_page_view | Page View | clinic_name, city, page_url | Pages & Screens |
| blog_scroll_50 | Scroll Trigger | page_title, scroll_percent, blog_category | Engagement Report |
| blog_scroll_90 | Scroll Trigger | page_title, scroll_percent, blog_category | Engagement Report |
| phone_number_clicked | Click Trigger | phone_number, page_name, button_location | Engagement Report |
| outbound_link_clicked | Link Click | destination_url, link_text, page_name | Events Report |

---

## GA4 Funnel Exploration

The booking journey will be configured in GA4 Funnel Exploration using the following sequence:

Landing Page

↓

booking_step_complete (Step 1)

↓

booking_step_complete (Step 2)

↓

booking_step_complete (Step 3)

↓

booking_completed

This setup enables the marketing team to analyse drop-offs between each booking step and optimise the booking experience accordingly.

---

## Google Ads Conversion

### Selected Conversion Event

**booking_completed**

### Why this event?

Although several user interactions are tracked, the completed booking represents the primary business objective. Importing this event into Google Ads allows campaigns to optimise for actual appointment bookings instead of micro-conversions such as phone clicks or WhatsApp clicks, resulting in better lead quality and improved return on ad spend.