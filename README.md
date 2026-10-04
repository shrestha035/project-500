# Pixel Perfect Display

Implement exactly the screenshot and nothing else

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/5d0e6253-e58d-4248-be45-36554acbaff1).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```

## Project 500 completion notes

This package includes the completed campaign flow: landing page, registration, cinematic random-piece unlock, 500-piece ticket puzzle, milestone clues, squad/referral sharing, WhatsApp community + QR, 499 state, 500 reveal, Golden Ticket explanation, project submission, and admin demo controls.

### Supabase setup
Run the SQL migration in `supabase/migrations/202610040001_project500.sql` against the Supabase project configured in `.env`. The migration creates `registrations`, `submissions`, `app_state`, and the atomic `register_builder` RPC that assigns one unique random piece per registration.

### Before launch
Replace the placeholders in `src/lib/config.ts` with the real WhatsApp Community URL and help number. Set `ADMIN_PASSCODE` in the deployment environment (the development fallback is `project500`).

### Demo
Open `/admin`, enable/set a demo count (184, 250, 400, 499, 500, etc.), then open `/unlock` to demonstrate the puzzle states. Demo values are explicitly labelled simulated data.
