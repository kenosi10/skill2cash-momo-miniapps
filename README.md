<img width="1920" height="1280" alt="image" src="https://github.com/user-attachments/assets/7f1b7ba5-2604-41a4-a398-fd4a7f78b6e6" />

# Skill2Cash

**Kasi Gig Escrow Mini App**  
*MoMo Mini App Hackathon 2026 – South Africa*

> **Tagline:** No more “I’ll pay you tomorrow”. Do the job. Get paid instantly.

---

### The Problem

In townships across South Africa (Hammanskraal, Mhluzi, Tembisa and beyond), the majority of youth rely on piece jobs — gardening, plumbing, hair braiding, phone repairs, cleaning.

There is almost zero trust:

- Clients fear paying upfront and getting a no-show  
- Workers fear finishing the job and hearing “come back tomorrow”  
- Cash is risky and leaves no record  
- No ratings, no proof, no digital footprint

Result: daily income is lost and informal workers stay invisible to the formal economy.

---

### The Solution

**Skill2Cash** is a Mini App that lives *inside* the MoMo app. No extra download. No heavy data usage.

**30-second flow:**

1. **Client posts & locks funds**  
   “Cut yard – R150 – 1975 Temba, Kudube Unit 2 – today 2pm”  
   → Pays via **MoMo Collections**. Money goes into escrow.

2. **Nearby worker accepts**  
   Verified youth within ~3 km gets notified and accepts the job.

3. **Job is done**  
   Worker uploads before & after photos as proof.

4. **Instant payout**  
   Client taps “Job Done” → **MoMo Disbursement** sends money straight to the worker’s MoMo wallet.

5. **Trust is built**  
   Both rate each other. Ratings + photo proof create a digital CV for informal workers.

---

### Why a MoMo Mini App?

- Lives where the money already is  
- Works on low data  
- Languages: English, isiZulu, Sepedi  
- Payment is locked by MTN → instant trust  
- USSD fallback planned for feature phones

---

### MoMo APIs Used

| API                        | Purpose                                      |
|---------------------------|----------------------------------------------|
| Collections               | Client locks job funds into escrow           |
| Disbursements             | Instant payout to worker                     |
| Transaction Status        | Confirm funds are locked before work starts  |
| Party Lookup / KYC        | Verify both parties are MoMo registered      |

**Escrow logic:** Funds are held in the merchant wallet and only released on client “Job Done” confirmation or admin dispute resolution.

---

### MVP Features

- Post a job (price, location, time, description)  
- Find jobs near me (geolocation)  
- “Funds Secured by MoMo” badge  
- Before / after photo proof  
- One-tap “Job Done” → instant payout  
- Simple rating system  

*Phase 2:* In-app chat + Dispute centre

---

### Tech Stack

- **Frontend:** MoMo Mini App SDK + React  
- **Backend:** Node.js + Supabase / Firebase  
- **Database:** Firestore (Jobs, Users, Ratings)  
- **Storage:** Firebase Storage (job proof photos)  
- **Payments:** MTN MoMo Sandbox (Collections + Disbursements)  
- **Hosting:** Azure Static Web Apps / MoMo Cloud

**Architecture**  
`MoMo Mini App → Backend (job + escrow state) → MTN MoMo API`  
`↳ Firestore (ratings & history)`

---

### Impact

- **Financial inclusion** – gives informal workers a transaction history and digital reputation  
- **Youth employment** – turns invisible skills into reliable daily income  
- **Stays in the MoMo ecosystem** – pay, lock, and payout never leave MoMo  
- **Scalable** – same problem exists in Ghana, Uganda, Zambia and other MoMo markets  
- Aligns with MTN’s vision: *“Don’t build another app. Build the next service millions access through MoMo.”*

---

### Roadmap

| Timeline              | Goal                                              |
|-----------------------|---------------------------------------------------|
| Hackathon (2–3 Sept)  | Working escrow flow in sandbox + 3 job categories |
| Month 1               | Pilot with 50 youth in Pretoria & Hammanskraal    |
| Month 3               | Dispute centre, Sepedi/Zulu, USSD support          |

---

### Team

**South Africa – Skill2Cash**

- **Tshepiso Tk Tsotetsi** – Product & Community Lead (Hammanskraal / Gauteng)

Currently looking for **1 Mobile Dev** + **1 Backend Dev** before the Johannesburg onsite (2–3 September).

---

### Run (Sandbox)

```bash
git clone https://github.com/kenosi10/skill2cash-momo-miniapps.git
cd skill2cash-momo-miniapps
npm install

# .env
MOMO_COLLECTIONS_SUBSCRIPTION_KEY=your_key
MOMO_DISBURSEMENT_SUBSCRIPTION_KEY=your_key
MOMO_TARGET_ENVIRONMENT=sandbox

npm run dev

![Pitch Slide](pitch_slide_fixed.png)
