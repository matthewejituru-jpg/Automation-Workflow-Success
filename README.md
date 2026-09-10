# De Volcano Assistant — WhatsApp AI Booking & Concierge Bot

An AI-powered WhatsApp assistant built for De Volcano Lounge & Suites, 
a lounge/suites business in Aba, Abia State, offering Executive Suites, 
a VIP Bar, Club Lava, Karaoke, and Grill services.

**Live demo:** [Whatsapp Number: +2347044502798]

## What it does
- Answers customer questions on room rates, bar/karaoke pricing, 
  amenities, and check-in/check-out times
- Handles booking and reservation requests end-to-end, including 
  collecting date, guest count, and service type
- Requires explicit customer confirmation before logging any booking
- Logs all confirmed bookings to a connected Google Sheet (append-only, 
  never overwrites existing records)
- Uses the customer's name naturally throughout the conversation without 
  overusing it
- Mirrors the customer's language, dialect, and tone while staying 
  professional
- Applies a controlled persuasion approach for hesitant customers — 
  addresses concerns once or twice, never pressures
- Escalates sensitive requests (refunds, cancellations, complaints) to 
  human staff rather than handling them directly
- Gatekeeps sensitive info like the business phone number, only sharing 
  it after a customer has explicitly asked multiple times

## Tech stack
- **n8n** — workflow automation and conversation logic
- **WAHA** — WhatsApp Web API integration
- **Google Sheets** — booking record-keeping

## How it works
Incoming WhatsApp messages are received via a WAHA webhook and routed 
through an n8n workflow. The assistant answers general questions directly 
from its knowledge of the business, and only triggers a booking flow on 
clear intent (e.g. "I want to book a suite"). Before any booking is 
logged, it sends the customer a summary and waits for explicit 
confirmation, then appends the confirmed booking as a new row in a 
Google Sheet — including guest count, service, date, and total price 
where known.

## Status
Demo build — created to showcase real-world automation and conversational 
AI design for a hospitality business use case.
