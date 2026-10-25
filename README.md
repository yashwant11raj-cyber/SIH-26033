# Smart India Hackathon Workshop

# Date: 25/10/2026

## Reference Number: 26006135

## Name: YASHWANT RAJ P

## Problem Title

SIH 26033: Multiple intermediaries reduce farmers earnings and increase consumer prices.

## Problem Creater's Organization

Ministry of Consumer Affairs, Food & Public Distribution

## Theme

Agriculture, FoodTech & Rural Development

## Problem Description

The Indian agricultural supply chain is highly fragmented, marred by a multi-layered ecosystem of intermediaries including village-level aggregators, commission agents (Arhtiyas), local wholesalers, and sub-wholesalers. Because individual smallholders generate small, isolated harvest volumes, they lack the leverage to sell directly to urban retail centers. Intermediaries exploit this lack of market access and real-time information asymmetry to capture disproportionate margins.
Consequently, farmers are deprived of fair earnings (often retaining less than 35-40% of the consumer spend), while urban retailers and end consumers face highly inflated prices. Furthermore, multiple manual handling stages delay transit timelines, precipitating substantial post-harvest structural food waste along the farm-to-fork journey.

## Proposed Solution

The proposed solution, Bolo-Kisan, introduces an interface-less smartphone app and an integrated Interactive Voice Response (IVR) telephone helpline tailored for smallholder farmers. The platform operates on a single-screen interface featuring only two large, colored graphic icons: [Call AI Helpdesk] and [Hold to Speak].
When a farmer streams a local voice note or speaks to the IVR line (e.g., "I have 5 bori of aloo ready in my village"), the backend architecture captures the network GPS coordinates and phone number automatically, eliminating registration forms. The unstructured regional audio payload is translated using deep language translation models.
A specialized semantic model identifies the agricultural variables (crop: potato, quantity: 5), maps the regional slang to localized unit weights (e.g., matching bori to exactly 50kg for that specific village pin code), and transforms it into a standardized metric format (250 kg).
The platform then aggregates these micro-quantities from neighboring smallholders within the same geographic cluster to create a bulk volume that matches the direct purchasing requirements of urban retailers on a unified B2B digital marketplace dashboard.

[Traditional System Configuration]
Smallholder Farmer ➔ Village Trader ➔ APMC Mandi Agent ➔ Central Wholesaler ➔ Sub-Wholesaler ➔ Urban Retailer

[Bolo-Kisan Unified Architecture]
Smallholder Farmer ➔ (Bolo-Kisan App Voice Note / IVR Line) ➔ AI Processing & Standardisation ➔ Direct Retailer

How it Addresses the Problem
• Collapses Multi-Tier Middleware: By serving as a single automated channel, it cuts out the 4 to 5 layers of agents, creating a direct transactional pathway from the village cluster point straight to the urban shop.
• Solves the Logistics Pooling Problem: Small-scale harvests fail to attract direct B2B corporate shipping due to high transport costs. This system groups small farm volumes into shared, cost-effective freight shipments, making direct distribution highly profitable.
• Removes Market Price Cheating: The system automatically references real-time baseline pricing directly from official government networks, ensuring middlemen cannot manipulate transaction valuations.

Innovation and Uniqueness of the Solution
• Zero-Friction Spoken Interface: Replaces text menus with a natural voice system designed specifically for users with zero digital literacy.
• Contextual Unit Transmutation Engine: The core software acts as an automated regional interpreter that parses village-specific counting configurations (bigha, bori, mann, tokri) and standardizes them server-side without user intervention.
• Triple-Lock Multi-Channel Voice Confirmation: To build immediate trust, the platform avoids text alerts. It uses automated voice playbacks inside the application, fires a localized automated telephone validation robot call, and sends an audio note summary straight to the farmer's WhatsApp interface.

## Technical Approach

Technologies to be Used
• Mobile & Voice Frameworks: Flutter (Optimized as an ultra-lightweight Progressive Web App under 5MB to execute smoothly on cheap, space-constrained Android units) along with Twilio/Exotel APIs for hosting toll-free IVR infrastructure.
• Core Backend Architecture: Python (FastAPI / Django Async workers) paired with PostgreSQL for spatial asset indexing and Redis for real-time inventory caching.
• Speech Processing & NLP Pipelines:
• Digital India BHASHINI Platform APIs to handle real-time Indic Speech-to-Text conversion across regional dialects.
• Fine-tuned Whisper AI models optimized for agricultural slang and noisy rural environments.
• Parameter Extraction Engine: Llama 3 (8B Instruct/Quantized) built with strict JSON-schema enforcement to cleanly isolate transactional variables.
• Live Price Discovery Interface: Official AGMARKNET Data API integrated to dynamically match baseline price indices.

## Feasibility and Viability

Analysis of the Feasibility of the Idea
• Technical Feasibility: High. The foundation uses stable, mature speech-to-text engines. Open APIs from Digital India BHASHINI handle regional Indian languages smoothly, and standard telecom infrastructures easily manage automated voice-loop confirmation services.
• Operational Feasibility: Relying on existing Farmer Producer Organization (FPO) setups allows the system to turn local collection points into natural aggregation yards, eliminating the need to build expensive new warehouses in every village.

Potential Challenges and Risks

1. Background Audio Distortions: Tractors, wind noise, and variations in local accents can disrupt voice processing accuracy.
2. High Shared-Freight Transit Costs: Direct delivery routes can become expensive if transport trucks have to make empty return trips.
3. Initial Trust Hurdles: Farmers may be hesitant to hand over physical harvest loads based solely on an automated digital confirmation.

Strategies for Overcoming These Challenges
• Noise Mitigation & Fallback Loops: Build audio-cleansing filters directly into the recording module while setting up the backend LLM to ask clarification questions if confidence metrics drop below 85%.
• Milk-Run Logistics Optimization: Implement specialized route-planning software to stitch multiple regional drop points into a continuous loop, keeping trucks running at peak capacity.
• FPO Human Validation Points: Keep the local FPO manager as the visible face of the network. Farmers drop goods off with a trusted neighbor, who uses a simple receipt-scanning feature to confirm the transaction on the spot.

## Impact and Benefits

Potential Impact on the Target Audience
• For Smallholder Farmers: Delivers an easy, transparent channel to sell crops directly at accurate market prices, bypassing traditional commission fees entirely from the comfort of their village.
• For Urban Retailers: Provides a direct, predictable way to source fresh farm produce without navigating crowded, multi-tiered city wholesale markets.

Benefits of the Solution
• Economic Benefit: Reclaims the 25% to 40% margin typically lost to middle-tier commissions, redistributing these gains to boost farmer payouts while lowering consumer shelf costs by 15-20%.
• Social Benefit: Empowers underserved smallholders who lack digital literacy, giving them equal access to broad national B2B buyer networks.
• Environmental Benefit (Food Waste Mitigation): Shifting from slow, multi-stage distribution networks to coordinated direct transport reduces handling delays, helping prevent rural food spoilage.

## Research and References

1. Official National Pricing Framework: Access the Agmarknet Portal to verify live daily mandi pricing structures across all Indian states.
2. National Translation Technology Portal: View the Digital India BHASHINI Mission Framework to review developer guidelines for speech-to-text integration in regional Indian languages.
3. National Open Data Repository: Utilize the open datasets available at data.gov.in to analyze national crop production metrics and regional trade volumes.
