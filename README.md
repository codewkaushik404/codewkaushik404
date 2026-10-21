<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?size=35&duration=3000&color=0E75B6&center=true&vCenter=true&width=900&lines=Hi,+I'm+Kaushik+K.S.;Backend+Engineer;Systems-Oriented+Full-Stack+Developer;Scalable+%7C+Secure+%7C+Performant+Systems" />
</p>

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=js,ts,java,python,nodejs,express,mongodb,postgres,mysql,docker,aws,vercel,git,github,react,tailwind,html,css,figma,postman,prisma&perline=11" />
  </a>
</p>

## About Me
I'm a Computer Science undergrad who enjoys building things and understanding how they work under the hood. I'm particularly interested in backend engineering, especially API design, database modelling, authentication and authorization, and building reliable server-side systems.

Through my projects and open-source contributions, including work on OpenLake's student platform at IIT Bhilai, I've worked on backend logic, data flow, and connecting different parts of an application. I like approaching problems from first principles, thinking through edge cases, and keeping systems simple, maintainable, and correct.

I'm looking to grow as a backend engineer by working on real engineering problems, taking ownership of features, and building software that holds up beyond the happy path.

---

## Open Source Contributions

**Summary:** 15 pull requests across 5 external repositories. 5 merged, 4 open and under review, 6 closed.

### OpenLake / Student_Database_COSA (Node.js, Express, MongoDB, React)

An institute-wide student database and workflow platform for IIT Bhilai's Office of Career and Student Affairs. I've been working on the **authentication, authorization, and workflow layers** of the backend, plus the matching frontend.

| PR | What I built | Status |
| --- | --- | --- |
| [#222: Refactor login/register + Zod validation](https://github.com/OpenLake/Student_Database_COSA/pull/222) | Replaced a broken Passport `User.register()` flow with manual, bcrypt-based login/registration. Moved DB and Passport config into a `config` module, centralized validation in `utils` using Zod, and enforced institute email-domain checks (`iitbhilai.ac.in`) at the schema level. | Open |
| [#223: `createBatch` endpoint + JWT middleware](https://github.com/OpenLake/Student_Database_COSA/pull/223) | Wrote an `isAuthenticated` middleware that verifies JWTs and attaches the user to `req.user`. Built the certificate-batch creation flow from scratch: role checks (only authorized club coordinators), organization hierarchy verification (Club → Council), **server-side approver resolution** so clients can't tamper with the approval chain, and Zod + DB existence checks on recipient IDs. | Open |
| [#232: Requests page components](https://github.com/OpenLake/Student_Database_COSA/pull/232) | Built a Requests page with reusable `Card` and `Requests` components and a reject modal wired into the request workflow. | Open |
| [#237: Hierarchical task assignment & progress tracking](https://github.com/OpenLake/Student_Database_COSA/pull/237) | Full-stack task management: backend schema and APIs, role-based visibility (assigners only see valid assignees), search/filter/sort, and a secure status-update flow where only the assigner can mark a task complete. | Open |

### OpenCodeChicago / hacktoberfest-2025-backend (Node.js, Express, MongoDB)

Hacktoberfest 2025 backend project. 3 PRs merged.

| PR | What I built | Status |
| --- | --- | --- |
| [#5: `GET /api/products/:id`](https://github.com/OpenCodeChicago/hacktoberfest-2025-backend/pull/5) | Product lookup endpoint with proper `400` (malformed ID) and `404` (not found) handling. | **Merged** |
| [#21: Modularize DB connection logic](https://github.com/OpenCodeChicago/hacktoberfest-2025-backend/pull/21) | Separated the MongoDB connection from the seed script so the server and seeding no longer overwrite each other's data. | **Merged** |
| [#54: Authentication, authorization & rate limiting](https://github.com/OpenCodeChicago/hacktoberfest-2025-backend/pull/54) | Signup/login with bcrypt hashing and `passport-local`, JWT-based stateless auth, a **custom configurable rate limiter** (request count and time window), and standard rate limits on sensitive routes such as login, signup, and products. | **Merged** |
| [#42](https://github.com/OpenCodeChicago/hacktoberfest-2025-backend/pull/42), [#44](https://github.com/OpenCodeChicago/hacktoberfest-2025-backend/pull/44): earlier iterations of JWT auth | Initial versions of the auth work, closed and superseded by #54. | Closed |

### angelabera / ShareBite

| PR | What I built | Status |
| --- | --- | --- |
| [#323: Google OAuth 2.0 with Passport.js + JWT](https://github.com/angelabera/ShareBite/pull/323) | Google sign-in with stateless JWT auth stored in an HTTP-only, secure cookie, plus callback and logout routes and a Mongoose user model supporting both local and Google providers. | Closed |
| [#274: User authentication (login/register)](https://github.com/angelabera/ShareBite/pull/274) | Registration, login, and logout flow with session handling and form validation. | Closed |

---

## Personal Projects

### [NoCron](https://github.com/codewkaushik404/NoCron) · [Live demo](https://no-cron.vercel.app)
A visual workflow automation platform for people who don't want to write cron jobs or hand-configure AWS services. Users build workflows by connecting nodes in a drag-and-drop editor, then deploy them as automated, serverless workflows. Workflow payloads are validated with Zod, stored in DynamoDB, and deployed to AWS Step Functions. Scheduled runs go through EventBridge Scheduler, emails through SES, and webhook endpoints are generated per workflow.
**Stack:** React, Recoil, Node.js, Express, Zod, AWS SDK · AWS Step Functions, EventBridge Scheduler, SES, DynamoDB, IAM

### [BetterTUF](https://github.com/codewkaushik404/BetterTUF)
A full-stack DSA learning platform for coding-interview prep. Problems are organized into structured sheets by topic and lecture, and users can track solved problems, schedule revisions, keep personal notes, and see progress at every level (sheet, topic, lecture).
**Stack:** React, TypeScript, Node.js, Express, PostgreSQL, Prisma, Zod

### [Node-Express-Auth](https://github.com/codewkaushik404/Node-Express-Auth)
A production-style authentication backend for MERN apps: signup, signin, and OTP verification, with JWT access and refresh tokens and **refresh-token rotation**. Includes session management and flexible logout, either from a single device or from all active sessions.
**Stack:** Node.js, Express, MongoDB, JWT

### [Roomify](https://github.com/codewkaushik404/Roomify-Hybrid-Ephemeral-chat-app)
A real-time, room-based chat app built directly on native WebSockets (the `ws` library, no Socket.IO). Users create and join rooms with instant updates, and messages are ephemeral, living only while the room is active. The architecture includes a room management system, a database for message storage, and a relay server for cross-instance communication.
**Stack:** React, Node.js, Express, `ws` (native WebSocket)

### [Geo-Spatial Proximity Filtering Engine](https://github.com/codewkaushik404/Geo-Spatial-Proximity-Filtering-Engine)
A location-based hotel search backend. It filters efficiently by price and availability, narrows candidates with geographic bounding boxes, and selects the Top-K nearest hotels using a Max Heap rather than sorting the full result set.
**Stack:** TypeScript, Node.js, Prisma, PostgreSQL

### [BlackJack-game](https://github.com/codewkaushik404/BlackJack-game)
A command-line Blackjack game that models card shuffling, betting, player hit/stand decisions, dealer logic, and win/loss calculation, including Blackjack payouts and ties.
**Stack:** TypeScript, Node.js, `prompt-sync`

---
## What I Work On

- **Authentication & authorization:** JWT access/refresh tokens with rotation, OAuth 2.0 (Google), Passport.js, bcrypt, OTP verification, session management, role-based access control
- **API design:** REST APIs, schema validation with Zod, consistent error handling, pagination, rate limiting
- **Backend architecture:** modular Express services, server-side enforcement of business rules, config and DB connection management, fail-fast startup
- **Data layer:** MongoDB / Mongoose, PostgreSQL with Prisma, DynamoDB, schema design, geo-spatial filtering
- **Real-time & cloud:** native WebSockets (`ws`), AWS Step Functions, EventBridge Scheduler, SES, IAM
- **Frontend:** React, Redux, Recoil, Tailwind
---

## Badges

![Holopin Badges](https://holopin.me/kaushikkanduri)
