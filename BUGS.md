# BUGS.md

## 1. QuotaExceededError on attendee registration
- **Issue**: `localStorage.setItem('attendees', ...)` threw `QuotaExceededError` when storage size exceeded.
- **Fix**: Added size check for screenshot (<100 KB). If the quota error occurs, fall back to storing a minimal attendee object (name, email, event, date) and log a warning. Updated `event_register.html` to handle this.
- **File Modified**: `event_register.html`

## 2. Duplicate event name entry in registration form
- **Issue**: After selecting an event from the event grid, the user was forced to re‑select the event name again.
- **Fix**: The selected event title is now stored in `localStorage['selectedEvent']` when clicking **Join Event**. The registration page reads this value, pre‑selects the option, and clears the temporary storage.
- **Files Modified**: `index.html`, `event_register.html`

## 3. "Watch Demo" button disabled
- **Issue**: The **Watch Demo** button linked to `#` and performed no action.
- **Fix**: Updated link to open the bundled video `Event_Management_Video_Generated.mp4` in a new tab.
- **File Modified**: `index.html`

## 4. "Don't have an account? Register" link pointed to event creation
- **Issue**: The login page sent users to the event creation page instead of the registration page.
- **Fix**: Corrected the hyperlink to point to `register.html`.
- **File Modified**: `login.html`

## 5. Admin role unable to create a new event
- **Issue**: Admin dashboard navigation did not redirect back after publishing an event, sending the user to the public dashboard.
- **Fix**: After event creation, redirect back to `admin.html` (admin dashboard) and keep the **Create New Event** link functional.
- **Files Modified**: `register.html`

## 6. Redirect after attendee registration
- **Issue**: Submitting the attendee registration form redirected to `index.html`, breaking the flow.
- **Fix**: Removed the redirect; the form now stays on the same page and updates the button text after successful registration.
- **File Modified**: `event_register.html`

## 7. Event selection loss after clicking **Join Event**
- **Issue**: Clicking **Join Event** on the home page did not retain the chosen event when reaching the registration form.
- **Fix**: Store selected event title in `localStorage['selectedEvent']` and pre‑select it on the registration page.
- **Files Modified**: `index.html`

---
All fixes have been applied and the application now works without the mentioned bugs.
