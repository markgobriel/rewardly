# Rewardly 🎁  
A full-stack loyalty program web app (think “PC Optimum”-style points) where users earn points on purchases, transfer points, and redeem them for discounts—backed by a role-based system for cashiers, managers, and superusers.

## 🔗 Live Demo  
- Web app: https://rewardly.vercel.app/

## ✨ What Rewardly Does  
Rewardly models a real loyalty system end-to-end: customers track their points + history, cashiers create/handle checkout flows, and managers audit activity and administer events/promotions.

## 👥 Roles & Capabilities  
- **Regular users**: view points balance, browse promos/events, RSVP, transfer points, and request redemptions.  
- **Cashiers**: create purchase transactions and process redemption requests.  
- **Managers**: verify/promote users, review all transactions, manage events & promotions, and resolve flagged activity.  
- **Superusers**: full privileges, including promoting users to managers/superusers.  

## 💳 Points, Transactions, and Redemptions  
Rewardly supports multiple transaction types and audit-friendly rules (e.g., transactions aren’t deletable):  
- **Purchase**: cashiers enter amount spent; points awarded by default (1 point per $0.25).  
- **Redemption**: users create a redemption request; cashiers process it at **$0.01 per point**.  
- **Transfer**: users can transfer points to other users.  
- **Adjustment**: managers can correct or reverse issues tied to earlier transactions.  
- **Event awards**: event organizers can award points to attendees.  

## 📅 Events & Promotions  
**Events**
- Managers create events, assign organizers, manage RSVPs/attendance, and allocate points for distribution.  
- Organizers award points to attendees and can edit event details (with some safety constraints).  

**Promotions**
- Managers create promo periods (e.g., boosted earn rates, optional minimum spend).  
- Managers can also set up “offer”-style promos that are single-use per user and applied at checkout.  

## 🧭 UX Highlights (Role-Based UI)  
- Clean **role-based navigation** so each user sees what they can actually do.  
- **React Router**-style navigation (URLs change properly; no “manual URL guessing”).  
- **QR codes** for (1) user identification (transfer/purchase) and (2) redemption request processing.  
- **Pagination + filters/sorting** on list-heavy pages (transactions, events, promotions, users).  

## 🧱 Tech Stack  
**Frontend**
- React + Vite
- Axios for API calls  

**Backend**
- Node.js + Express REST API for the loyalty system  
- Prisma ORM + SQLite database  
- JWT-based auth (jsonwebtoken / express-jwt)  

## 🔐 Authentication & Security (High-Level)  
- Login-protected endpoints using JWTs  
- Role-based access control: permissions enforced by role (“regular”, “cashier”, “manager”, “superuser”).  

## 🗺️ Roadmap Ideas  
- Smarter anomaly/suspicious cashier heuristics + manager review UX  
- Admin analytics dashboards (earn vs redeem trends, promo effectiveness)  
- Third-party integration for bonus features (e.g., email/SMS confirmations, receipts)

## 🤝 Collaborators  
- [Chifeng Wang](https://github.com/Chifiwang)  
- [Salman Husainie](https://github.com/Just-Call-Sal)  

## 🙏 Credits  
Built as a full-stack loyalty program project (backend foundation + role-based web experience).
