# Booking System
REST API Backend-system byggt med **Spring Boot** och **Spring Security**. Systemet hanterar rumstyper, bokningar, användarroller och använder **JWT** för säker autentisering.

## Projektöversikt

Detta system är utvecklat som en del av en skoluppgift och implementerar ett hotellbokningssystem med följande funktioner:

- CRUD-operationer för bokningar
- Rollbaserad åtkomstkontroll (USER/ADMIN)
- JWT-autentisering
- In-memory datalagring
- Avancerad felhantering med custom exceptions

## Teknologier

- **Java 17**
- **Spring Boot 3.2.x**
- **Spring Security** (JWT + Basic Auth)
- **Maven** - byggverktyg
- **Validation** - input-validering

## Projektstruktur
com.hotel.booking/
├── BookingSystemApplication.java
├── config/
│ ├── JwtFilter.java # JWT-valideringsfilter
│ ├── JwtUtil.java # JWT-generering och validering
│ └── SecurityConfig.java # Spring Security-konfiguration
├── controller/
│ ├── AuthController.java # /login-endpoint
│ ├── BookingController.java # Boknings-endpoints
│ └── GlobalExceptionHandler.java # Central felhantering
├── dto/
│ ├── BookingRequest.java
│ ├── LoginRequest.java
│ └── LoginResponse.java
├── exception/
│ ├── BookingNotFoundException.java
│ ├── GuestCapacityException.java
│ └── RoomFullyBookedException.java
├── model/
│ ├── Booking.java
│ ├── ErrorResponse.java
│ └── RoomType.java
└── service/
└── BookingService.java


### Bokningar

| Metod | Endpoint | Beskrivning | Roll |
|-------|----------|-------------|------|
| GET | `/api/bookings` | Lista alla bokningar | ADMIN |
| POST | `/api/bookings` | Skapa ny bokning | USER |
| DELETE | `/api/bookings/{id}` | Radera bokning | ADMIN |

## Testanvändare

| Användarnamn | Lösenord | Roll |
|--------------|----------|------|
| user | user123 | USER |
| admin | admin123 | ADMIN |

## Installation och körning
Förutsättningar
Java 17 eller högre
Maven 3.6+


### 👤 Författare: 
Syedur Rahman - Skoluppgift i Java/Spring Boot
