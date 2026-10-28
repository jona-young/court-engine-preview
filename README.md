# Court Booking Engine: rules preview

**[Live demo →](https://jona-young.github.io/court-engine-preview/)**

An interactive demo from a court booking platform I built for racquet clubs. Clubs set their booking policy as configurable rules instead of code: booking limits, doubles-only peak hours, stricter limits after a no-show. This page lets you switch those rules on and off and see straight away which courts a test member can still book, and why.

<img width="763" height="1199" alt="Screenshot 2026-10-28 at 11 32 14 AM" src="https://github.com/user-attachments/assets/55852c1b-16b7-4a75-a32e-fde8c60906bc" />

## Highlights

- **Rules engine:** written in pure TypeScript with no framework dependencies, so the same code checks bookings on the server and runs this demo in the browser. Rules are scoped (club, facility, sport, court, membership tier, member), and a more specific rule can replace a broader one.
- **Explains itself:** every time slot shows which rule passes or blocks it, and the member sees a plain-language reason instead of a greyed-out button.
- **Time handling:** opening hours are local wall-clock times, bookings are stored in UTC, and daylight saving time is handled.
- **One codebase:** the React components come from the production Next.js app and are built into this static site with Vite. A GitHub Actions workflow publishes them here, separate from the private source.

<img width="746" height="365" alt="Screenshot 2026-10-28 at 11 33 28 AM" src="https://github.com/user-attachments/assets/de4238a3-ca36-4617-8441-d4f50d0bf548" />

**Stack:** TypeScript, React, Next.js, Tailwind CSS and Vite. The full platform runs on Payload CMS and PostgreSQL.

<sub>This repository holds only the built preview (HTML, CSS and JavaScript). It is published automatically from a private repository.</sub>
