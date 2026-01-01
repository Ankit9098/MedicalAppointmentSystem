# Medical Appointment Management System (ASP.NET Core MVC)

A full-stack ASP.NET Core MVC web application that allows **Patients** to request appointments, **Doctors** to approve/reject and manage schedules, and **Admins** to manage doctors/patients/appointments. Built with **C#**, **Razor Views**, **SQL Server**, **ADO.NET**, **stored procedures**, and **Bootstrap**.

## Screenshots
> Add images to a `/screenshots` folder and update paths below.

- Patient Dashboard  
  ![Patient Dashboard](screenshots/patient_dashboard.png)

- Doctor Schedule  
  ![Doctor Schedule](screenshots/doctor_schedule.png)

- Admin Dashboard  
  ![Admin Dashboard](screenshots/admin_dashboard.png)

## Features
### Patient
- Register / Login / Logout
- Search doctors (specialty/location)
- Request an appointment (date/time + reason)
- View upcoming and past appointments
- Cancel upcoming appointments

### Doctor
- View schedule and pending requests
- Approve / Reject appointments
- Mark appointments as Completed
- Add optional notes

### Admin
- Manage doctors (Create/Update/Deactivate)
- View all patients
- View all appointments
- Dashboard metrics (appointments today, pending approvals, etc.)

## Tech Stack
- **C#**
- **ASP.NET Core MVC** (Razor Views)
- **SQL Server**
- **ADO.NET**
- **Stored Procedures**
- **Bootstrap**
- **Git/GitHub**

## Database
This project uses SQL Server with stored procedures.

### Tables
- Users
- Doctors
- Patients
- Appointments

### Setup
1. Create a new SQL Server database (example: `MedicalAppointmentsDB`)
2. Run the scripts in:
   - `docs/DatabaseSchema.sql`
   - `docs/StoredProcedures.sql`
3. Update the connection string in `appsettings.json`

Example `appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=YOUR_SERVER;Database=MedicalAppointmentsDB;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}
