# Ekan Solutions Inc.

## Current State
The site has 9 pages: Home, About, Services, Solutions, and 5 individual service landing pages (Cybersecurity, Project Management, Full Stack Development, AWS Cloud Solutions, Java Development, QA/Testing). Navigation uses a `page` state in App.tsx. Services overview page lists all 6 service cards with "Learn More" links.

## Requested Changes (Diff)

### Add
- New `AIServicesPage.tsx` component — a full dedicated landing page for "AI & Automation Services"
- Page sections:
  1. Hero — "Intelligent Automation for the Modern Enterprise" with trust badges and dual CTAs
  2. 6 Capability cards — AI Consulting & Strategy, Machine Learning Development, NLP & Conversational AI, Process Automation (RPA), Predictive Analytics, AI Integration & APIs
  3. Tech stack — Python, TensorFlow, PyTorch, OpenAI, LangChain, Hugging Face, Azure AI, AWS SageMaker, Apache Spark, Power BI
  4. 5-Step Process — Discovery & Assessment → AI Strategy → Model Development → Integration & Testing → Monitoring & Optimization
  5. CTA banner with consultation button and phone number
- New "AI & Automation" card added to ServicesPage.tsx with "Learn More" button
- New nav entry in desktop + mobile header (Services dropdown or added to Services page access)
- Add `"aiservices"` page type to App.tsx page union and conditional rendering

### Modify
- `App.tsx`: Add `"aiservices"` to page union type, import AIServicesPage, add conditional render
- `ServicesPage.tsx`: Add AI & Automation as a 7th service card

### Remove
- Nothing

## Implementation Plan
1. Create `src/frontend/src/components/AIServicesPage.tsx` with hero, capability cards, tech stack, process steps, and CTA
2. Update `App.tsx` — import AIServicesPage, add `"aiservices"` to type union, add conditional render
3. Update `ServicesPage.tsx` — add AI & Automation card with setPage("aiservices") on Learn More
