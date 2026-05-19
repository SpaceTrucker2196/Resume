## Professional Summary  

Highly experienced IT professional with over 25 years across multiple platforms, including **native iOS and Android development, REST APIs, Graph API, enterprise authentication, networking, and IT infrastructure**. Specialized in **native mobile app development** with 10+ years of expertise and a strong commitment to **test-driven development**. Proven record in **optimizing infrastructure, reducing costs, and leading complex projects**. Certified in **ITIL** and well-versed in IT Service Management (ITSM) environments.  

Currently shipping **CareTime**, a one-tap activity tracker for paid family caregivers in Self-Directed Support programs that exports GT Independence–compliant PDF timesheets — built natively for both iOS (Swift/SwiftUI/SwiftData) and Android (Kotlin/Jetpack Compose/Room), with iOS as the behavioral source of truth and a 1:1 unit test parity rule between platforms (22 XCTest suites mirrored by 30 JUnit suites covering segment lifecycle, EVV status, SHA-256 audit chain, PBKDF2 PIN hashing, and PDF rendering). Zero third-party dependencies on either side.  

Also building and operating OpenClaw agents to manage 5 real-world rental units. A rental operations agent develops custom leases, handles local government compliance and licensing, and searches for local landlord and homeowner programs related to energy efficiency and building improvements. Tenants can communicate via email with an agent dedicated to their unit for any questions regarding their rental, but each tenant is sandboxed to their own context — tenants cannot ask questions beyond the scope of their rental, and the agent will never return information pertaining to other tenants. A suite of automated tests enforces compliance with these boundaries.  

Interested in careers with organizations that provide **direct services to public needs** such as disability services, recovery organizations, and healthcare.  

---

## Experience  

### River.io LLC — *Owner / Mobile, Infrastructure & DevOps Engineering*  
**Sept 2025 – Present**  

**Cross-platform mobile (iOS + Android), test-driven**  
- Designed and shipped **CareTime**, a native iOS app (Swift 5.10 / SwiftUI / SwiftData) for paid family caregivers in Self-Directed Support programs — one-tap activity tracking that exports GT Independence–compliant PDF timesheets, with EVV (Electronic Visit Verification) including location capture at clock-in/out, participant attestation, and a tamper-evident SHA-256 audit hash chain.  
- Ported CareTime to native **Android** (Kotlin 2.0 / Jetpack Compose / Material 3 / Room / Hilt / WorkManager / Glance widgets) — idiomatic Kotlin, not literal Swift translation, while preserving observable behavior exactly (sub-30 s discard, single-active-segment invariant, midnight split, PBKDF2 PIN hashing at 210 000 iterations).  
- Operate a **parity workspace** with audit-driven workflow: every iOS service has a 1:1 Kotlin counterpart, and every iOS unit test (22 XCTest suites) has a matching JUnit test on Android (30 JVM test suites) — drift is caught by audit prompts and logged in a parity log rather than papered over.  
- Built **MaterialsAndPractices**, a universal iPhone/iPad iOS app (SwiftUI + Core Data with CloudKit sync via `NSPersistentCloudKitContainer`) for small-scale organic farms — USDA-sourced plant cultivar database, grow management, soil health monitoring with pH spectrum and lab integration, agricultural lease management with payment tracking, worker time tracking with overtime detection, FDA FSMA harvest safety checklists, and full traceability of organic amendments. English + Spanish localization. Recently restored 14 previously-quarantined XCTest suites and re-aligned per-entity Core Data helpers.  
- **Zero third-party dependencies on both platforms** — Apple frameworks only on iOS; AndroidX + Google + Hilt + Room only on Android. No Retrofit, Glide, Moshi, RxJava, Firebase, etc.  
- Live Activities and Siri Shortcuts on iOS; segment-aware foreground notifications and zero-parameter App Shortcuts on Android.  
- **Engineering posture: compiled, native languages over cross-platform UI frameworks.** Choose C / C++ / Swift / Objective-C / Kotlin over Flutter, React Native, and Electron because native code gives smaller binaries, lower memory and battery cost, direct access to platform APIs (Live Activities, Glance widgets, `nl80211`, SwiftData, Room, CloudKit) without bridge layers, real platform UX, and longer supportability — no framework treadmill, no abandoned plugin ecosystems, and full first-party debugging/tooling. The price (writing each platform twice) is paid back in correctness, performance, and durability; the test-parity workspace keeps the two ports honest.  

**Security / systems engineering**  
- Designed and built **sloth**, a passive WiFi and network security analysis tool in **C99** (Linux, ncurses + libpcap + `nl80211`) — 23 live views including 802.11 beacon/probe/deauth sniffing, ARP/mDNS/NBNS/DHCP/SSDP device discovery, TLS ClientHello / **JA3 fingerprint** capture, DNS/QUIC/HTTP observation, and synthesized alerts (port scans, deauth floods, NXDOMAIN bursts, threat-intel hits, periodic beaconing).  
- Sloth never injects packets, scans, or modifies kernel state — it is a fully passive forensic tool. JSONL forensic log and per-alert pcap output for downstream analysis.  
- Backed by **50 C unit tests** covering the protocol parsers (TLS/QUIC/HTTP/ARP/deauth), threat-intel matcher, connection tracker, and rule engine, with a `fake_platform` shim so kernel-facing code is testable on any host.  
- Ported a Swift-based password generator to **pure C11** (MeowPasswordC) with full Debian packaging, man pages, CMake build system, and an automated release pipeline publishing `.deb` packages to GitHub Releases.  

**AI / DevOps infrastructure**  
- Architected and managed a **multi-agent AI operations platform** on a cloud VPS, orchestrating three specialized AI agents with isolated workspaces, dedicated models, and automated cron-based workflows.  
- Designed GitHub Actions workflows for build, test, package, and release across multiple repositories with auto-versioning release pipelines.  
- Configured **10+ automated cron jobs** handling real estate deal scanning, property management, weather reporting, security audits, backups, and CISA vulnerability monitoring.  

---

### VARC Inc. — *IT Specialist*  
**Nov 2024 – Aug 2025**  
- Automated Microsoft 365 user administration (account provisioning, manager assignments, group memberships, license management) with descriptive error handling and fail-safes.  
- Developed custom Copilot agents to support HR and IT workflows.  
- Reduced repetitive administrative tasks, saving staff time and minimizing errors.  
- Improved IT operations consistency through PowerShell automation and Microsoft Graph integration.  

---

### Cosanti Foundation — *Information Technology Manager*  
**Jun 2021 – Sept 2024**  
- Managed network infrastructure across two Arizona sites (Cosanti and Arcosanti) using Ubiquiti UniFi.  
- Oversaw vendor relationships (Lumen, Adobe, Autodesk, Google, and more).  
- Migrated company web presence to Dreamhost, saving $5K+ monthly.  
- Led VoIP migration, saving $2.5K monthly.  
- Directed fiber and network upgrades at the historic Cosanti site.  
- Upgraded wiring to Cat 6 shielded cable to solve lightning-related issues.  
- Created training documentation for long-term maintenance.  

---

### Lead iOS Developer  
**Jan 2021 – Aug 2023**  
- Developed **AgPilotX**, an agricultural aviation guidance system for iPads.  
- Implemented Swift + MVVM integration with aircraft hardware, including Bluetooth/Wi-Fi controls, valve systems, and heads-up displays.  

---

### Haulynx — *Senior iOS Developer*  
**Jul 2019 – Nov 2020**  
- Contributed to a logistics app for long-haul truckers (electronic driver logs, load management).  
- Implemented CI/CD with Bitrise.  
- Integrated Splunk and Amplitude for user insights.  
- Led migration from Firebase to AWS GraphQL DB.  

---

### General Motors — *Consultant*  
**Aug 2018 – May 2019**  
- Built test infrastructure and automated delivery systems for the Maven car-sharing app.  
- Introduced new testing protocols with Nimble/Quick.  
- Improved deployment with Concourse CI.  

---

### GPS Insight — *Lead Mobile Developer*  
**Jan 2016 – Aug 2018**  
- Led the redesign and complete rewrite of the core iOS app in eight months.  
- Served as designer and lead developer for asset-tracking apps with Google Maps.  

---

### AAA Insurance — *Development Anchor*  
**Apr 2015 – Dec 2015**  
- Led a team of six building iOS and Android apps for AAA customers.  
- Partnered with Pivotal Labs to retain BDD and rapid delivery practices with Spring Boot.  

---

### Charles Schwab — *Senior Software Engineer*  
**Oct 2011 – Dec 2014**  
- Developed native iPhone/iPad IT service management clients.  
- Built Splunk-based dashboards for operational intelligence.  

---

### Ashley Furniture Industries — *Senior Developer*  
**Dec 2009 – May 2011**  
- Developed and launched the **iAshley iPad sales catalog app** for 500+ sales reps and stores.  

---

### DHL — *Principal Systems Engineer*  
**Mar 2004 – May 2009**  
- Developed sales and tracking apps for BlackBerry OS, streamlining operations.  

---

### Cosanti Foundation — *Webmaster*  
**Sept 2001 – Mar 2004**  
- Designed and maintained [arcosanti.org](http://www.arcosanti.org).  

---

### Software Developer (Various Roles)  
**1992 – 2001**  
- Held programmer/developer roles at **IBM, State of Washington, Target Stores, and Thomson Reuters**.  

---

## Education & Certifications  

- **Stanford University** — Online Courses in Software Engineering (2010)  
- **Hewlett Packard** — ITIL V3 Foundation Certification (2008, 2016)  
- **Sun Microsystems** — J2EE Certification (2000)  
- **Minneapolis College of Art and Design** — Digital Media Design (1999–2001)  
- **Winona State University** — B.A. in Liberal Arts (1988–1992)  

---
