# School Migration Hub - Android App

A comprehensive Android application for school digital migration management, built with modern Android development practices using Kotlin, MVVM architecture, Room database, and real-time features.

## 🚀 Features

### Authentication & User Management
- **Login/Register**: Email and Google OAuth authentication
- **Role-based Access**: Student, Teacher, Admin, and Parent roles
- **Profile Management**: User profiles with image upload
- **Security**: Encrypted local storage and session management

### Class Management
- **Create Classes**: Teachers can create and manage classes
- **Join Classes**: Students join via enrollment codes or QR codes
- **Class Details**: View class information, students, and materials
- **Add/Remove Students**: Dynamic class enrollment management
- **Class Analytics**: Attendance rates, assignment completion

### Live Classes & Video Calling
- **WebRTC Integration**: Real-time video calls for classes
- **Screen Sharing**: Teachers can share screens during lessons
- **Recording**: Live class recording capabilities
- **Chat**: In-class messaging during live sessions
- **Participant Management**: Host controls for managing attendees

### Attendance Tracking
- **Digital Attendance**: QR code and location-based check-ins
- **Manual Marking**: Teachers can manually mark attendance
- **Attendance Reports**: Generate detailed attendance analytics
- **Real-time Updates**: Instant attendance synchronization
- **Parent Notifications**: Automated attendance alerts

### Assignment Management
- **Create Assignments**: Rich assignment creation with due dates
- **File Attachments**: Support for various file types
- **Submission Tracking**: Monitor assignment completion
- **Grading System**: Points-based grading with feedback
- **Late Submissions**: Automatic late submission handling

### Payment Integration
- **Multiple Gateways**: Razorpay and Stripe integration
- **Fee Management**: School fees, course payments
- **Payment History**: Complete transaction records
- **Receipt Generation**: Digital receipts and invoices
- **Payment Reminders**: Automated payment notifications

### Time Management
- **Class Schedules**: Integrated calendar system
- **Assignment Deadlines**: Deadline tracking and reminders
- **Live Class Timing**: Scheduled and instant live classes
- **Notification System**: Time-based alerts and reminders

## 🏗️ Architecture

### MVVM Pattern
- **Model**: Data classes and repository pattern
- **View**: Activities and Fragments with data binding
- **ViewModel**: Business logic and UI state management

### Database (Room)
- **Local Storage**: Offline-first architecture
- **Sync**: Background synchronization with server
- **Migrations**: Automatic database schema updates

### Networking
- **Retrofit**: RESTful API communication
- **WebSocket**: Real-time features
- **WebRTC**: Peer-to-peer video calling

### Dependency Injection
- **Hilt**: Compile-time dependency injection
- **Modular**: Clean separation of concerns

## 📱 Key Activities & Fragments

### Authentication Flow
- `SplashActivity` - App startup and session check
- `LoginActivity` - User authentication
- `RegisterActivity` - New user registration

### Main Application
- `MainActivity` - Bottom navigation container
- `ClassesFragment` - Class management interface
- `AssignmentsFragment` - Assignment overview
- `AttendanceFragment` - Attendance tracking
- `LiveClassesFragment` - Video calling interface
- `PaymentsFragment` - Payment management

### Detailed Views
- `LiveClassActivity` - Full-screen video calling
- `PaymentActivity` - Payment processing
- `ClassDetailsActivity` - Individual class management
- `AssignmentDetailsActivity` - Assignment view and submission

## 🛠️ Technical Implementation

### Real-time Features
```kotlin
// WebRTC Implementation
class LiveClassViewModel {
    fun initializeWebRTC(context: Context, userId: String, userName: String, 
                        liveClassId: String, isHost: Boolean) {
        // WebRTC peer connection setup
        // Camera and microphone access
        // Video/audio streaming
    }
}
```

### Payment Processing
```kotlin
// Razorpay Integration
class PaymentActivity : PaymentResultListener {
    override fun onPaymentSuccess(razorpayPaymentID: String?) {
        // Update payment status
        // Send confirmation
        // Generate receipt
    }
}
```

### Attendance System
```kotlin
// QR Code Attendance
class AttendanceFragment {
    private fun scanQRCode() {
        // Camera permission
        // QR code scanning
        // Location verification
        // Attendance marking
    }
}
```

### Live Class Management
```kotlin
// Video Call Controls
class LiveClassActivity {
    fun toggleCamera() { /* Camera on/off */ }
    fun toggleMicrophone() { /* Mic mute/unmute */ }
    fun shareScreen() { /* Screen sharing */ }
    fun recordClass() { /* Recording start/stop */ }
}
```

## 🔐 Security Features

- **Data Encryption**: Local database encryption
- **Secure Storage**: SharedPreferences encryption
- **Network Security**: HTTPS/TLS communication
- **Authentication**: JWT token management
- **Permission Management**: Runtime permission handling

## 📊 Analytics & Reporting

- **Attendance Reports**: Detailed attendance analytics
- **Payment Tracking**: Financial transaction reports  
- **Class Performance**: Assignment and participation metrics
- **User Activity**: Login and engagement tracking

## 🚀 Setup Instructions

### Prerequisites
- Android Studio Arctic Fox or later
- Android SDK 24+
- Kotlin 1.8+
- Java 8+

### Installation
1. Clone the repository
2. Open in Android Studio
3. Sync Gradle dependencies
4. Configure API keys in `local.properties`:
   ```properties
   RAZORPAY_KEY=your_razorpay_key
   FIREBASE_API_KEY=your_firebase_key
   BASE_URL=https://your-api-server.com
   ```
5. Build and run the application

### Database Setup
The app uses Room database with automatic migrations. First run will create the database schema automatically.

### API Integration
Configure the backend server URL in `build.gradle` or `local.properties` for API communication.

## 🔧 Configuration

### Build Variants
- **Debug**: Development build with logging
- **Release**: Production build with ProGuard

### Dependencies
- AndroidX libraries
- Room database
- Retrofit networking
- WebRTC for video calls
- Razorpay/Stripe for payments
- Glide for image loading
- Hilt for dependency injection

## 📱 Supported Features by Role

### Students
- Join classes via enrollment codes
- View assignments and submit work
- Attend live classes
- Check attendance records
- Make payments for courses

### Teachers  
- Create and manage classes
- Take attendance (QR/manual)
- Create and grade assignments
- Conduct live classes
- Generate reports

### Admins
- Manage all classes and users
- View system-wide analytics
- Handle payment disputes
- Configure app settings

### Parents
- View child's attendance
- Monitor assignment progress
- Receive notifications
- Make payments

## 🎯 Future Enhancements

- **Offline Mode**: Enhanced offline functionality
- **AI Integration**: Smart scheduling and recommendations
- **Multi-language**: Localization support
- **Advanced Analytics**: Machine learning insights
- **Integration APIs**: Third-party service connections

This Android application provides a complete school management solution with modern features, real-time capabilities, and a user-friendly interface designed for educational institutions transitioning to digital platforms.
