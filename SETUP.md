# Fensho Website Setup

A beautiful seller registration platform built with Next.js, Tailwind CSS, and Supabase.

## Features

- Modern, responsive home page with hero section
- Vendor registration form with validation
- Thank you page after successful submission
- Data persistence with Supabase
- Clean, professional design with emerald color theme

## Setup Instructions

### 1. Configure Environment Variables

Copy `.env.local` and add your Supabase credentials:

```bash
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
```

You can find these values in your Supabase project dashboard under Settings > API.

### 2. Database Setup

The database migration has already been applied. It creates a `vendor_registrations` table with the following fields:

- name
- phone
- email
- pickup_address
- pincode

The table has Row Level Security (RLS) enabled:
- Public users can submit registrations
- Only authenticated users can view submissions

### 3. Run the Development Server

```bash
npm run dev
```

Visit `http://localhost:3000` to see the website.

## Pages

- `/` - Home page with hero section and features
- `/vendor` - Vendor registration form
- `/thank-you` - Success page after form submission

## Tech Stack

- Next.js 13 (App Router)
- TypeScript
- Tailwind CSS
- shadcn/ui components
- Supabase
- Lucide React icons
