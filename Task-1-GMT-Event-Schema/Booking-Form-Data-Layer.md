# Booking Form dataLayer Events

## Booking Funnel Tracking

The appointment booking process consists of three steps.

Google Tag Manager cannot automatically detect movement between these steps. Therefore, the front-end developer must manually trigger a dataLayer push whenever a user successfully completes each step.

GTM listens for these events and forwards them to GA4.

---

## Step 1 – Clinic & Specialty Selected

```javascript
window.dataLayer = window.dataLayer || [];

window.dataLayer.push({
  event: "booking_step_complete",
  step_number: 1,
  step_name: "location_specialty_selected",
  clinic_location: "Bengaluru - Indiranagar",
  specialty: "Orthopaedics"
});
```

---

## Step 2 – Patient Details Submitted

```javascript
window.dataLayer.push({
  event: "booking_step_complete",
  step_number: 2,
  step_name: "patient_details_entered",
  patient_name: "Rahul Sharma",
  preferred_date: "2026-07-10",
  phone_last4: "5678"
});
```

---

## Step 3 – Booking Confirmed

```javascript
window.dataLayer.push({
  event: "booking_step_complete",
  step_number: 3,
  step_name: "booking_confirmation",
  booking_status: "confirmed",
  appointment_type: "Consultation"
});
```

---

## Final Booking Event

```javascript
window.dataLayer.push({
  event: "booking_completed",
  booking_id: "BK102458",
  clinic_location: "Bengaluru - Indiranagar",
  specialty: "Orthopaedics",
  appointment_date: "2026-07-10"
});
```

---

# GA4 Funnel Exploration

1. booking_step_complete (step_number = 1)
2. booking_step_complete (step_number = 2)
3. booking_step_complete (step_number = 3)
4. booking_completed

This funnel enables the marketing team to identify where users abandon the booking process and calculate drop-off rates between each step.



