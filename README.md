Skill2Cash - Kasi Gig Escrow | MoMo Mini App Hackathon 2026

Team: South Africa-Skill2Cash

    Tagline: No more "I will pay you tomorrow". Do the job, get paid instantly.

MoMo API

Track
[blocked]
Status
[blocked]
Made for
[blocked]
The Problem

In townships like Mhluzi, Hammanskraal and across SA, 60% of youth do piece jobs - gardening, plumbing, hair braiding, phone repairs. There is zero trust:

    Clients fear paying upfront and getting a no-show
    Youth fear working and hearing "come tomorrow"
    No proof, no ratings, cash handling is risky
    Word of mouth only = no digital footprint

Result: Daily income is lost, youth stay invisible to the formal economy.
The Solution

Skill2Cash is a Mini App that lives INSIDE the MoMo app (no extra download).

How it works - 30 second flow:

    Client Posts & Locks: "Cut yard R150, 1975 Temba kudube unit 2, today 2pm" - Pays R150 via MoMo Collections into escrow. Money is safe.
    Youth Accepts: Verified youth within 3km gets push, accepts job.
    Do The Job: Youth arrives, does job, uploads before/after photo in mini-app.
    Instant Payout: Client taps "Job Done" -> MoMo Disbursement pays youth INSTANTLY to MoMo wallet.
    Trust Built: Both rate each other. Disputes reviewed with photos.

Why MoMo Mini App?

    No download, no data-heavy app - lives where money already is
    Works low-data, USSD fallback planned
    Languages: English, isiZulu, Sepedi
    Instant trust because payment is locked by MTN

MoMo APIs Used
API	Usage
Collections (Collection Widget)	Client locks job funds into escrow wallet
Disbursements	Instant payout to worker after client approval
Transaction Status	Verify escrow locked before worker starts
Party Lookup / KYC	Verify both users are MoMo registered

Escrow Logic: Funds held in merchant wallet -> Released only on JobDone confirmation or admin dispute resolution.
Key Features (MVP)

    Post Job with price, location, time
    Find Jobs near me (geolocation)
    Escrow payment badge - "Funds Secured by MoMo"
    Before/After photo proof
    One-tap "Job Done" & instant payout
    Rating system - building digital CV for informal workers
    In-app chat (Phase 2)
    Dispute center (Phase 2)

Tech Stack

    Frontend: MoMo Mini App SDK, HTML5, JavaScript (React)
    Backend: Node.js + Supabase / Firebase (Auth, Realtime DB, Storage)
    Database: Firestore - Jobs, Users, Ratings
    Storage: Firebase Storage - Job proof photos
    APIs: MTN MoMo Sandbox (Collections, Disbursements)
    Hosting: Azure Static Web Apps / MoMo Cloud

Architecture

Client App (MoMo Mini App) -> Supabase (Job Logic + Escrow State) -> MTN MoMo API
                                   |
                                   -> Firestore (Ratings, History)

How To Run (Sandbox)
bash

# Clone
git clone https://github.com/skill2cash/momo-miniapps.git

# Install
npm install

# Add .env
MOMO_COLLECTIONS_SUBSCRIPTION_KEY=your_key
MOMO_DISBURSEMENT_SUBSCRIPTION_KEY=your_key
MOMO_TARGET_ENVIRONMENT=sandbox

# Run
npm run dev

Demo Video (Coming Soon)

Link to 2-min demo to be added after sandbox access
Impact - Why It Wins Track 1: Everyday Essentials

    Financial Inclusion: Gives informal workers transaction history & digital CV
    Youth Employment: Turns invisible skills into daily income
    Stays in Ecosystem: Money never leaves MoMo - pay, escrow, payout all inside
    Scalable: Same problem in Ghana, Uganda, Zambia - MoMo markets
    Aligns with MTN Vision: "Don't build another app. Build the next service millions access through MoMo."

Team - South Africa-Skill2Cash

    Tshepiso Tk Tsotetsi - Product & Community Lead (Hammanskraal / Gauteng)

Open to adding 1 Mobile Dev + 1 Backend Dev before Sept 2-3 onsite in Johannesburg.
Roadmap

Hackathon 24hrs (Sept 2-3, JHB): Working escrow flow in sandbox + 3 job categories
Month 1: Pilot with 50 youth in Pretoria & Hammanskraal
Month 3: Add dispute center, Sepedi/Zulu, USSD for feature phones
License

MIT - Built for MoMo Mini App Hackathon 2026

Contact: For MoMo Developer Team - Ready for sandbox keys and mentorship. Let's kill cash risk in kasi.
