# Bookify  — Beauty Salon Booking App

An Android mobile application that simplifies the process of booking beauty and grooming services, connecting clients with salons and stylists in their area.

---

##  Overview

Bookify was developed as a bachelor's thesis project at the **"1 Decembrie 1918" University of Alba Iulia**, Faculty of Computer Science and Engineering (2025).

The app addresses a common pain point in the Romanian market: booking appointments at beauty salons still relies heavily on phone calls, waitlists, and manual coordination. Bookify streamlines this into a few taps, giving users real-time availability, stylist selection, and integrated payment.

---

##  Features

- **Authentication** — Register/Login with email & password, Google Sign-In, or Facebook Sign-In (via Firebase Authentication)
- **Browse & Search** — Explore salons and stylists by category (Hair, Manicure, Skincare, Makeup, etc.), filtered by proximity using geolocation
- **Stylist Profiles** — View detailed stylist profiles, services offered, and pricing
- **Real-time Booking** — Select a date from an interactive calendar and choose from live available time slots
- **Appointment Management** — View, modify, or cancel bookings from a dedicated screen
- **Payment Integration** — Pay at the salon (cash) or securely through **Google Pay**
- **Booking History** — Track confirmed, cancelled, and paid appointments with full details

---

##  Tech Stack

| Layer | Technology |
|---|---|
| Language | Java |
| Architecture | MVVM (Model–View–ViewModel) |
| UI Framework | Android Jetpack (Fragments, Navigation, LiveData, ViewModel, RecyclerView) |
| UI Design | Material Design Components |
| Backend / Database | Firebase Firestore |
| Authentication | Firebase Authentication |
| Payments | Google Pay API (sandbox) |
| Build System | Gradle |

---

##  Architecture

The project follows the **MVVM** architectural pattern, ensuring a clear separation of concerns:

- **Model** — Data entities: `Salon`, `Stylist`, `Service`, `Booking`, `TimeSlot`, `Category`
- **ViewModel** — Business logic and reactive data via `LiveData` (e.g. `HomeViewModel`, `SearchViewModel`)
- **View** — Activities and Fragments handling UI and user interaction

Data persistence is handled entirely through **Firebase Firestore**, accessed directly from ViewModels for simple operations or through dedicated service classes for more complex workflows.

---

##  App Screens

<img width="360" height="760" alt="image" src="https://github.com/user-attachments/assets/3f60b206-ae34-44f3-ac73-be06c437cd45" />


---

##  Getting Started

### Prerequisites

- Android Studio (latest stable version recommended)
- Android SDK 21+
- A Firebase project with Firestore and Authentication enabled
- Google Pay API credentials (for payment testing)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/beauty-booking-app/beauty-booking-app.git
   cd beauty-booking-app
   ```

2. **Connect Firebase**
   - Go to [Firebase Console](https://console.firebase.google.com/) and create a project
   - Add an Android app and download `google-services.json`
   - Place it in the `app/` directory

3. **Configure Google Pay**
   - Follow the [Google Pay Android integration guide](https://developers.google.com/pay/api/android/overview)
   - The app runs in **sandbox mode** by default — no real transactions are processed

4. **Build & Run**
   - Open the project in Android Studio
   - Sync Gradle and run on an emulator or physical device (Android 5.0+)

---

## 🔮 Future Improvements

- **Push notifications** via Firebase Cloud Messaging (reminders 24h and 2h before appointments, with snooze/cancel actions)
- **Reviews & ratings** — clients can rate services and stylists, with aggregated scores displayed on profiles
- **Calendar export** — sync bookings to Google Calendar or Outlook via API
- **Salon admin portal** — a web dashboard or in-app admin module for salon owners, featuring sales stats, booking trends, and staff management

---

## 📚 References

- [Firebase Authentication Docs](https://firebase.google.com/docs/auth)
- [Firebase Firestore Docs](https://firebase.google.com/docs/firestore)
- [Google Pay Android API](https://developers.google.com/pay/api/android/overview)
- [Android Jetpack Architecture Components](https://developer.android.com/topic/architecture)
- [Material Design Components for Android](https://m2.material.io/components?platform=android)

---

## 👩‍💻 Author

**Eligia Răileanu**  
Faculty of Computer Science and Engineering  
"1 Decembrie 1918" University of Alba Iulia  
Coordinator: Lect. univ. dr. Daniela Nagy-Onița  
© 2025
