# HealthCareApplication_Backend
dme · MDCopyHealthCare AB — Booking Application Backend

A RESTful backend API for a healthcare booking system built with Java and Spring Boot
.
Patients can book appointments with healthcare providers. Authentication is handled via JWT stored in HttpOnly cookies.

Tech Stack

Java 17
Spring Boot 3.3.5

MongoDB (database)

Spring Security + JWT (jjwt 0.11.5)
Maven

JUnit 5 + Mockito (testing)

JaCoCo (code coverage — minimum 80%)

OWASP Dependency Check (security scanning)

GitHub Actions (CI/CD)

# Prerequisites
Before running the project you need:

Java 17 installed

Maven installed

MongoDB running locally on port 27017

Git

API Endpoints
Authentication
MethodEndpointDescriptionAccessPOST/auth/registerRegister a new userPublicPOST/auth/loginLogin and receive JWT cookiePublicPOST/auth/logoutLogout and clear cookieAuthenticatedGET/auth/checkCheck authentication statusAuthenticated

Availability

MethodEndpointDescriptionAccessPOST/availability/createCreate a time slotPROVIDERGET/availability/allGet all available slotsAuthenticatedPUT/availability/{id}Update a time 

slotPROVIDERDELETE/availability/{id}Delete a time slotPROVIDER

Appointments

MethodEndpointDescriptionAccessPOST/appointment/createBook an appointmentPATIENT

User Roles

RoleDescriptionPATIENT Can view availability and book appointmentsPROVIDERCan create and manage time slotsADMINFull access
