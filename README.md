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
<img width="386" height="766" alt="image" src="https://github.com/user-attachments/assets/b7163be2-5eea-415b-92f6-64920ac8bb7f" />
<img width="315" height="667" alt="image" src="https://github.com/user-attachments/assets/6114bb36-7b1b-4eb0-9643-ab428346152b" />
<img width="304" height="642" alt="image" src="https://github.com/user-attachments/assets/be05b181-5f99-4833-8216-e56d7ff65a63" />
<img width="359" height="761" alt="image" src="https://github.com/user-attachments/assets/cd614b90-343c-456c-a4f1-79f3f342cc2a" />
<img width="360" height="760" alt="image" src="https://github.com/user-attachments/assets/4a1799a5-d3a1-4e53-be11-28e7f97edf9a" />
<img width="382" height="804" alt="image" src="https://github.com/user-attachments/assets/595f4e97-8044-46c5-b59c-1031ce5b4d93" />
<img width="372" height="784" alt="image" src="https://github.com/user-attachments/assets/19efd537-2755-4b8c-aed5-df68c65dcf6f" />
<img width="382" height="804" alt="image" src="https://github.com/user-attachments/assets/6ed067dd-8e9b-451f-a5d6-db167bd72bd0" />
<img width="371" height="785" alt="image" src="https://github.com/user-attachments/assets/9d3705fc-e5c6-4cae-bf9f-e5bebd85e259" />
<img width="372" height="788" alt="image" src="https://github.com/user-attachments/assets/eea2baa8-08a2-4505-8d4e-1c9feef26c22" />
<img width="360" height="788" alt="image" src="https://github.com/user-attachments/assets/3def5acb-b518-4a83-8cbe-9498ddbe2bed" />
<img width="319" height="673" alt="image" src="https://github.com/user-attachments/assets/d2f149c3-2bd4-459b-af54-7aa8cd0072a8" />
![Uploading image.png…]()




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
