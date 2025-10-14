# PushPress Workflow Setup Guide
## Smart Routing System Implementation

### 🎯 **Overview**
This guide provides step-by-step instructions for setting up PushPress workflows that automatically route prospects based on their experience level and goals.

### 📋 **Required Workflows**

#### **Workflow 1: New to CrossFit Pipeline**
**Trigger:** Contact tagged with "New to CrossFit"
**Purpose:** Route beginners to No Sweat Intro consultation

**Setup Steps:**
1. **Create New Workflow** in PushPress
2. **Name:** "New to CrossFit - No Sweat Intro"
3. **Trigger:** Contact Tag Added "New to CrossFit"
4. **Actions:**
   - Send welcome email with No Sweat Intro information
   - Schedule No Sweat Intro appointment reminder
   - Add to "New Member" nurture sequence
   - Set follow-up reminder for 24 hours before appointment

**Email Template:**
```
Subject: Welcome to Trident Athletics - Your No Sweat Intro is Next!

Hi [First Name],

Thanks for reaching out to Trident Athletics! Since you're new to CrossFit, we've set you up for a No Sweat Intro - a free 30-minute consultation where one of our coaches will:

• Discuss your fitness goals
• Show you around our facility
• Create a personalized plan
• Answer all your questions

No workout, no pressure - just clarity and planning!

Your consultation is scheduled for [Date] at [Time] at 410 Calvert Ave, Alexandria, VA.

What to bring: Just yourself and questions!

Looking forward to meeting you,
The Trident Athletics Team
```

#### **Workflow 2: Experienced Athlete Pipeline**
**Trigger:** Contact tagged with "Experienced Athlete"
**Purpose:** Fast-track experienced athletes to appropriate programs

**Setup Steps:**
1. **Create New Workflow** in PushPress
2. **Name:** "Experienced Athlete - Program Matching"
3. **Trigger:** Contact Tag Added "Experienced Athlete"
4. **Actions:**
   - Send program information email
   - Offer drop-in booking or program consultation
   - Add to "Experienced Athlete" nurture sequence
   - Set follow-up reminder for 3 days

**Email Template:**
```
Subject: Welcome to Trident Athletics - Let's Match You with the Perfect Program!

Hi [First Name],

Awesome! With your fitness background, you'll appreciate our championship-level coaching and community.

You have two great options:

1. **Drop-in to a class** - $30, arrive 15 minutes early to sign waiver
2. **Program consultation** - Quick goal review to match you with the perfect program

Our programs include:
• CrossFit Classes (all levels)
• Olympic Weightlifting
• Master Weightlifting Club
• Performance Lab
• Personal Training

Ready to get started? Book your drop-in or consultation here: https://api.grow.pushpress.com/widget/bookings/trident-bookings

Looking forward to training with you,
The Trident Athletics Team
```

#### **Workflow 3: Drop-in Pipeline**
**Trigger:** Contact tagged with "Drop-in" or "Local Prospect"
**Purpose:** Handle drop-in bookings and comp week offers

**Setup Steps:**
1. **Create New Workflow** in PushPress
2. **Name:** "Drop-in & Comp Week"
3. **Trigger:** Contact Tag Added "Drop-in" OR "Local Prospect"
4. **Actions:**
   - Send class schedule and waiver information
   - Provide payment options (online link or in-person)
   - Send confirmation and preparation details
   - Set follow-up reminder for day after visit

**Email Template:**
```
Subject: Ready to Try Trident Athletics? Here's Everything You Need!

Hi [First Name],

Perfect! For local folks wanting to try us out, you have two great options:

**Option 1: Drop-in to any class - $30**
• Arrive 15 minutes early
• Sign waiver and pay at gym
• Jump right into class!

**Option 2: Free comp week**
• Experience our community for a full week
• Try different classes and programs
• See what it's like to be part of Trident

Class Schedule: [Link to schedule]
Waiver: [Link to online waiver]
Payment: [Link to online payment]

Choose your adventure! We can't wait to meet you.

The Trident Athletics Team
```

#### **Workflow 4: Out-of-Town Guest Pipeline**
**Trigger:** Contact tagged with "Out-of-Town Guest"
**Purpose:** Handle visiting athletes and guests

**Setup Steps:**
1. **Create New Workflow** in PushPress
2. **Name:** "Out-of-Town Guest - Drop-in"
3. **Trigger:** Contact Tag Added "Out-of-Town Guest"
4. **Actions:**
   - Send online payment link and class schedule
   - Provide local recommendations (restaurants, hotels)
   - Send confirmation and preparation details
   - Set follow-up reminder for day after visit

**Email Template:**
```
Subject: Welcome to Alexandria! Ready to Train at Trident?

Hi [First Name],

We love having visitors! Our drop-in rate is $30 per class.

**Two ways to pay:**
1. Online now: [Payment Link]
2. At the gym: Arrive 15 minutes early

**What to know:**
• Class Schedule: [Link to schedule]
• Location: 410 Calvert Ave, Alexandria, VA
• Parking: Street parking available
• What to bring: Just yourself and workout clothes!

**While you're in town:**
• Great restaurants nearby: [Local recommendations]
• Hotels: [Hotel recommendations]

Ready to train? We can't wait to meet you!

The Trident Athletics Team
```

### 🏷️ **Required Tags Setup**

Create these tags in PushPress:
- **New to CrossFit**
- **Experienced Athlete**
- **Drop-in**
- **Local Prospect**
- **Out-of-Town Guest**

### 📊 **Automation Rules**

#### **Auto-Tagging Rules:**
1. **If contact mentions "new to CrossFit" or "never done CrossFit"** → Tag "New to CrossFit"
2. **If contact mentions "CrossFit experience" or "competitive athlete"** → Tag "Experienced Athlete"
3. **If contact mentions "visiting" or "out of town"** → Tag "Out-of-Town Guest"
4. **If contact mentions "try out" or "drop in"** → Tag "Drop-in"

#### **Follow-up Sequences:**
- **New to CrossFit:** 5-email sequence over 14 days
- **Experienced Athlete:** 3-email sequence over 7 days
- **Drop-in:** 2-email sequence over 3 days
- **Out-of-Town Guest:** 2-email sequence over 3 days

### 📅 **Calendar Integration**

#### **No Sweat Intro Slots:**
- **Duration:** 30 minutes
- **Available times:** Weekdays 9 AM - 7 PM, Saturdays 8 AM - 11 AM
- **Buffer time:** 15 minutes between appointments
- **Coach assignment:** Rotate between available coaches

#### **Drop-in Classes:**
- **All regular class times available**
- **Capacity:** Regular class capacity minus 2 spots for drop-ins
- **Waiver requirement:** Must be signed before class starts

### 📱 **Mobile App Integration**

#### **Booking Widgets:**
- **No Sweat Intro:** https://api.grow.pushpress.com/widget/bookings/trident-bookings
- **Annual Upgrade:** https://api.grow.pushpress.com/widget/bookings/annual-upgrade
- **Dad Bod Strong:** https://api.grow.pushpress.com/widget/bookings/dad-bod
- **Embed on website:** Yes
- **Mobile responsive:** Yes
- **Payment integration:** Yes

#### **Waiver System:**
- **Online waiver:** Required for all participants
- **Mobile-friendly:** Yes
- **Auto-sync:** With contact records
- **Expiration:** 1 year from signing

### 📈 **Success Metrics Tracking**

#### **Key Performance Indicators:**
- **No Sweat Intro conversion rate:** Target 60%+
- **Drop-in to member conversion:** Target 25%+
- **Workflow completion rate:** Target 90%+
- **Response time:** Under 2 minutes during business hours

#### **Reporting Dashboard:**
- **Daily workflow performance**
- **Tag application accuracy**
- **Conversion rates by category**
- **Staff workload distribution**

### 🔧 **Testing Checklist**

#### **Before Going Live:**
- [ ] Test all workflows with sample contacts
- [ ] Verify email templates render correctly
- [ ] Confirm calendar integration works
- [ ] Test booking widget functionality
- [ ] Verify waiver system integration
- [ ] Check mobile responsiveness
- [ ] Test payment processing
- [ ] Confirm auto-tagging rules work
- [ ] Verify follow-up sequences trigger correctly
- [ ] Test staff notifications

#### **Post-Launch Monitoring:**
- [ ] Monitor workflow performance daily
- [ ] Check tag application accuracy
- [ ] Review conversion rates weekly
- [ ] Gather staff feedback monthly
- [ ] Optimize based on results

### 🚀 **Expected Results**

With this smart routing system:
- **90%+ routing accuracy** to appropriate experience
- **80%+ No Sweat Intro conversion** to members
- **70%+ drop-in return rate** for additional visits
- **50% reduction** in staff routing questions
- **Improved prospect experience** with faster, more accurate routing

This system ensures every prospect gets the right introduction to Trident Athletics based on their experience level and goals, leading to higher satisfaction and better conversion rates!
