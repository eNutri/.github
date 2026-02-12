# eNutri Roadmap & Sustainability Plan

## Short summary
This document summarises the current state of eNutri, our limitations, and our strategic roadmap for technical development and long-term sustainability. It outlines how eNutri will continue to evolve as a research tool while maintaining its core mission of providing accessible, open-source dietary assessment and personalized nutrition advice.

## Sustainability & Governance

### Vision
eNutri is committed to being a sustainable, community-driven research platform. We aim to:
- Return open-source accessibility for researchers and developers globally
- Ensure long-term platform stability through thoughtful technical architecture
- Support ongoing maintenance through clear governance and community contribution
- Build capacity within the research community through documentation and training

### Funding & Support
eNutri's sustainability can be supported through multiple channels:
- Community-led improvements and localizations (translations, food databases for different regions)
- Research Software Maintenance Fund (RSMF) from Software Sustainability Institute (https://www.software.ac.uk/programmes/research-software-maintenance-fund)
- Research grants and funding from UKRI, Horizon Europe, and open-source sustainability initiatives supporting open-source research tools

### Maintenance Strategy
5. **Community Support:** Active community support through GitHub issues, discussions, and email contact

### Strategic Priorities

**1. Technical Modernization & Maintainability**
- Migrate from deprecated AngularJS (end-of-life since 2021) to Angular 21 with TypeScript
- Upgrade Firebase Realtime Database to Firestore for better scalability and querying
- Implement automated testing, CI/CD pipelines, and Infrastructure as Code (IaC)
- Document codebase comprehensively for future developers and contributors
- Simplify data export format to harmonize with other dietary assessment tools (e.g., Intake24)
- Enable self-service deployment through automated scripts and IaC in Google Cloud

**2. Knowledge Transfer & Training**
- Develop comprehensive training materials in multiple formats (video, written, interactive)
- Create deployment guides for researchers to manage their own eNutri instances in their Google Cloud accounts
- Design eNutri to be accessible and inclusive for diverse user populations (ethnic/cultural diets, dietary restrictions, lower-income groups, varied technology proficiency)

## Limitations (current)
- The frontend is implemented in **AngularJS (1.x)**, which is end-of-life and no longer actively maintained. This creates multiple issues:
  - Harder to find engineers with recent AngularJS experience; most new developers learn modern frameworks (React, Vue, Angular 2+)
  - Security and dependency updates are limited; third-party packages and build tools may be outdated
  - Tooling and ecosystem: modern dev tools, linters, and testing frameworks have better support for newer frameworks
  - Performance and code modularity: AngularJS lacks many of the component-driven patterns and performance optimisations available in modern frameworks

### Short-term plan
- Document and freeze stable public interfaces (API endpoints and database structure) to reduce breaking changes
- Add automated tests around critical flows (authentication, FFQ submission, backend triggers) to make refactors safer
- Plan infrastructure for scalable, independent deployment by external researchers

### Medium-term plan
- Conduct user research with existing researcher community to identify usability improvements and pain points
- Migrate to **Angular 21** as the modern framework, chosen for its strong ecosystem, component architecture, and developer experience
- Improve developer onboarding with setup scripts, local Docker development, and comprehensive architecture documentation
- Enable researchers to independently deploy and manage their own eNutri instances without software developer support
- Establish eNutri as a widely-adopted tool in UK dietary research alongside complementary tools (e.g., Intake24)

### Long-term goals
- Achieve WCAG 2.2 accessibility standards for all users, including older adults and those with varying technology proficiency
- Foster a vibrant, diverse community of researchers sharing best practices and knowledge around eNutri
- Create a contributor network of software developers making enhancements and adaptations for different research contexts
- Support use of eNutri in diverse research areas including underrepresented populations and health conditions
- Ensure eNutri remains a sustainable, reliable, and secure research tool for decades to come, supporting UK and international research

## eNutri's Unique Value
- **Unique personalised nutrition capability** - only tool offering automated, food-based dietary advice using evidence-based diet quality scores
- **Complements existing tools** like Intake24 (24-hour recalls) and legacy tools like EPIC-Norfolk (paper-based FFQ from 1990s)
- **Scalable digital assessment** - improves on time-consuming manual methods and outdated paper questionnaires
- **Researcher-friendly** - automates data analysis and reduces manual data entry burden
- **Evidence-based** - scientifically-validated outputs giving researchers confidence in data quality

eNutri's past and current user base includes:
- **GutBrain study** (gut bacteria and brain function research)
- **Sustainable Food Systems**: Research on dietary patterns and environmental impact
- **Healthy Ageing**: Dietary assessment in older adult populations with accessibility considerations

## Phased Migration Plan: AngularJS to Angular 21

This section outlines the development strategy for creating a new Angular 21 version of eNutri while maintaining active support for current AngularJS-based projects.

### Overview
eNutri will develop a new Angular 21 version while maintaining current AngularJS-based projects in a stable state:
- **Current projects** continue running on AngularJS with critical bug fixes and security updates only (development paused)
- **New Angular 21 version** developed and tested independently over ~9 months
- **Focus:** Complete rebuild of all features in Angular 21 with improved UX and architecture

### Phase 0: Preparation & Infrastructure (Months 1-3)

**Objectives:** Establish foundation for new Angular 21 version while strengthening researcher community engagement

**Key Activities:**

**AngularJS Stabilization & Researcher Support**
- Lock AngularJS codebase to stable version (no new features)
- Conduct interviews and observations with existing researcher-users to identify usability challenges and priorities
- Document all current data models, API endpoints, business logic, and deployment procedures
- Create comprehensive test suite for existing functionality
- Establish maintenance-only mode with focus on critical bug fixes and security updates
- Continue supporting current research projects without disruption

**Angular 21 Infrastructure & Accessibility Foundation**
- Set up Angular 21 monorepo with TypeScript strict mode
- Configure webpack/build tools, linting, and code quality standards
- Establish CI/CD pipeline with GitHub Actions (separate from AngularJS)
- Set up automated testing infrastructure (Jest for unit tests, Cypress for E2E)
- Plan for WCAG 2.2 accessibility compliance from the ground up

**Documentation & Community Engagement**
- Setup local development environments with Docker for both versions
- Document AngularJS business logic, user workflows, and researcher requirements for rebuild
- Create reference specifications for all modules and components from user perspective
- Plan community engagement strategy, including online access request form and feedback mechanisms
- Develop Code of Conduct and contribution guidelines for open-source collaboration

**Deliverables:** 
- Angular 21 project skeleton with build/test pipeline
- API compatibility specifications
- Complete documentation of AngularJS functionality for rebuild
- Team trained and ready for development
- AngularJS codebase in stable maintenance mode

**Duration:** 3 months (Months 1-3)

### Phase 1: Foundation Development (Months 4-6)

**Objectives:** Build core infrastructure and low-complexity modules in Angular 21

**Modules to Develop (Priority Order):**
- **Effort:** 2-3 weeks
- **Benefits:** 
  - Demonstrates Angular 21 development success early
  - Foundation for all other modules
  - Independent of other features
- **Approach:**
  - Build new Angular 21 authentication module
  - Implement against Firestore (new backend storage)
  - Full test coverage (unit + E2E)
 **Complexity:** High (foundation for all features)
 **Effort:** 4-6 weeks
 **Benefits:**
  - Better scalability and querying capabilities where Firestore is adopted
  - Comprehensive API testing
  - Ensure seamless support for new Angular 21 instances
- **Effort:** 2-3 weeks
- **Benefits:**
  - Accelerates development of remaining modules
  - Consistent UI/UX across all features
  - Maintainability and code reuse
**Effort:** 6-7 weeks
**Objectives:** Rebuild core researcher-facing features prioritized by user research from Phase 0

**User Research Insights:** Phase 0 interviews with existing researcher-users will identify key pain points. Likely priorities based on historical feedback:
- Dashboard filtering and sorting for study management
- Interoperable data exports (aligning with Intake24 format and FAIR principles)
- Clearer researcher admin configuration interface
#### 2.1 Researcher Dashboard (Module Priority: HIGH)
- **Scope:** Study management, participant tracking, progress monitoring

#### 2.2 Data Export & Report Generation
- **Benefits:**
  - Harmonize with Intake24 format
  - Reduce manual post-processing for researchers
  - Enable better interoperability

#### 2.3 Admin Configuration Panel
- **Scope:** Study setup, consent forms, screening questions, FFQ configuration
- **Complexity:** Medium-High
- **Effort:** 6-7 weeks

### Phase 2: Core Features Development (Months 7-9)

**Objectives:** Rebuild core researcher-facing features prioritized by user research from Phase 0

**User Research Insights:** Phase 0 interviews with existing researcher-users will identify key pain points. Likely priorities based on historical feedback:
- Dashboard filtering and sorting for study management
- Interoperable data exports (aligning with Intake24 format and FAIR principles)
- Clearer researcher admin configuration interface
- Self-service training materials for independent deployment

**Modules to Develop:**

#### 2.1 Researcher Dashboard (Module Priority: HIGH)
- **Scope:** Study management, participant tracking, progress monitoring
- **Complexity:** High (complex UX, lots of state management)
- **Effort:** 6-8 weeks
- **Impact:** Critical for researcher experience

#### 2.2 Data Export & Report Generation
- **Scope:** Excel/CSV export functionality, data formatting
- **Complexity:** Medium
- **Effort:** 4-5 weeks
- **Benefits:**
  - Harmonize with Intake24 format
  - Reduce manual post-processing for researchers
  - Enable better interoperability

### Phase 3: Advanced Features & Beta Release (Months 8-9)

**Modules to Migrate:**

#### 3.1 Food Frequency Questionnaire (FFQ) UI
- **Scope:** Main data collection interface for participants
- **Complexity:** Very High (largest component, complex interactions)
- **Effort:** 8-10 weeks for core FFQ functionality targeted for Beta in Months 8-9; additional refinements (up to 10-14 weeks total) may continue as post-release maintenance
- **Risk Level:** High (affects core functionality)

#### 3.2 Personalized Nutrition Advice UI
- **Scope:** Results presentation, diet quality score display, recommendations
- **Complexity:** Medium
- **Effort:** 4-6 weeks

#### 3.3 User Account Management
- **Scope:** Profile settings, preferences, notification settings
- **Complexity:** Low-Medium
- **Effort:** 2-3 weeks

### Phase 4: Release & Dual Maintenance (Month 9: Release & ongoing maintenance)
**Objectives:** Release Angular 21 version, support dual-version environment, transition projects

**Release & Maintenance Strategy:**
- **Angular 21 Version:** Production-ready release, ongoing feature enhancements and new capabilities
**Deliverables:**
- Angular 21 production release

**Technical Metrics:**
- Test coverage > 80% for all modules
- Bundle size < 500KB (gzipped)
- Researcher satisfaction with new Angular 21 interface (target: >= current version or higher)
- FFQ completion rate in new version >= AngularJS version

### Phase Exit Criteria

**Phase 0 → Phase 1 (Month 3 → 4):** 
- ✓ Backend APIs fully functional
- ✓ Common UI components stable and tested
- ✓ All core modules functional (dashboard, data export, FFQ)
- ✓ Beta testing with researchers completed
- ✓ Migration tools developed
- ✓ Documentation complete

**Impact Metrics During Development (9-month period):**
- Elimination of deprecated libraries and security vulnerabilities
- Automated deployment reduces time to launch new instances (target: <1 hour for trained researcher)
- Test coverage > 80% for all modules

**Post-Release Impact Metrics:**
- Number of distinct research groups independently deploying Angular 21 version
- Growth in researcher-user base
- Number of research publications citing eNutri
- Community contributions and external issue/feature requests
- Adoption of eNutri for new research areas

**Sustainability Indicators:**
- Continuous flow of research support through UKRI, H2020, and other major funders using eNutri
- Active community of researcher-users sharing knowledge and best practices
- Growing contributor network extending eNutri for diverse research contexts

**Long-term Sustainability Strategy:**
- eNutri's value as a research enabler ensures continued interest and use across UK research community
- Training materials and clear documentation support independent deployment, reducing ongoing support burden
- Governance structure and Code of Conduct foster contributor network for maintenance and enhancement
- Commitment to modern development practices (automated testing, CI/CD, IaC) reduces future maintenance costs
- Positioning as the modern, evidence-based UK FFQ with personalized nutrition capabilities ensures long-term research relevance
