# Trident Athletics Smart Routing Framework
## AI Bot Routing System for Optimal Member Experience

### 🎯 **Routing Objectives**
Route every prospect to the right experience based on their fitness level and goals, ensuring they get the appropriate introduction to Trident Athletics.

### 📊 **Routing Decision Tree**

```
PROSPECT CONTACTS TRIDENT
         ↓
    EXPERIENCE LEVEL?
    ┌─────────────────┐
    │  NEW TO FITNESS │ → NO SWEAT INTRO (30-min consult)
    │  NEW TO CROSSFIT│
    └─────────────────┘
           ↓
    EXPERIENCED ATHLETE → DIRECT TO APPROPRIATE PROGRAM
           ↓
    WHAT'S THEIR GOAL?
    ┌─────────────────┐
    │  TRY OUT GYM    │ → DROP-IN PROCESS
    │  JOIN GYM       │ → FREE COMP WEEK
    │  OUT-OF-TOWN    │ → $30 DROP-IN
    └─────────────────┘
```

### 🔍 **Experience Level Detection Questions**

#### **For Fred (Voice AI Bot) - Quick Assessment:**
- "Are you brand new to CrossFit, or have you trained before?"
- "What's your fitness background - are you new to working out or do you have experience?"
- "Have you done any functional fitness or strength training before?"

#### **For Tommy (Conversation Bot) - Detailed Discovery:**
- "What's been your fitness journey so far?"
- "Have you tried CrossFit or similar functional fitness before?"
- "What kind of training are you most comfortable with?"

### 🎯 **Routing Categories & Responses**

#### **1. NEW TO FITNESS / NEW TO CROSSFIT**
**Route to:** No Sweat Intro (30-minute consultation)
**Trigger:** First-time fitness experience or new to CrossFit

**Response Script:**
"You're exactly who we love working with! Since you're new to this type of training, we'll set you up with a No Sweat Intro - it's a free 30-minute consultation where one of our coaches will discuss your goals, show you around the gym, and create a personalized plan. No workout, no pressure - just clarity and planning."

**PushPress Workflow:**
- Tag: "New to CrossFit"
- Schedule: No Sweat Intro appointment
- Follow-up: 24-hour preparation email
- Next step: Free comp week after successful intro

#### **2. EXPERIENCED ATHLETE / EXPERIENCED IN CROSSFIT**
**Route to:** Appropriate program or drop-in
**Trigger:** Has CrossFit experience or competitive athletic background

**Response Script:**
"Awesome! With your experience, you'll appreciate our coaching and community. You can either drop into a class for $30 (arrive 15 minutes early to sign waiver) or we can set up a quick goal review session to match you with the perfect program."

**PushPress Workflow:**
- Tag: "Experienced Athlete"
- Options: Drop-in booking or program consultation
- Fast-track: Direct to appropriate class level

#### **3. TRY OUT GYM / LOCAL PROSPECT**
**Route to:** Free comp week or drop-in
**Trigger:** Local person wanting to try the gym

**Response Script:**
"Perfect! For local folks wanting to try us out, you can either drop into any class for $30 (just arrive 15 minutes early to sign the waiver and pay), or we can set you up with a free comp week to really experience our community. Which sounds better to you?"

**PushPress Workflow:**
- Tag: "Local Prospect"
- Options: Free comp week signup or drop-in booking
- Follow-up: Comp week preparation or drop-in confirmation

#### **4. OUT-OF-TOWN GUEST**
**Route to:** $30 drop-in process
**Trigger:** Visiting from out of town

**Response Script:**
"We love having visitors! Our drop-in rate is $30 per class - you can either come to the gym and pay there (arrive 15 minutes early to sign the waiver), or I can send you a link to pay online ahead of time. What works better for you?"

**PushPress Workflow:**
- Tag: "Out-of-Town Guest"
- Options: Online payment link or in-person payment
- Follow-up: Drop-in confirmation and class schedule

#### **5. DAD BOD STRONG INTEREST**
**Route to:** Dad Bod Strong consultation
**Trigger:** Men 38-55 interested in transformation program

**Response Script:**
"Perfect! Dad Bod Strong is our 6-month transformation program designed specifically for men 38-55 who want to rebuild strength, energy, and confidence. It combines Andrea's championship coaching with Chriss's mental toughness approach. You can book your consultation here: https://api.grow.pushpress.com/widget/bookings/dad-bod"

**PushPress Workflow:**
- Tag: "Dad Bod Strong Interest"
- Book consultation: https://api.grow.pushpress.com/widget/bookings/dad-bod
- Follow-up: Program information and success stories

#### **6. ANNUAL UPGRADE INTEREST**
**Route to:** Annual membership upgrade consultation
**Trigger:** Current members interested in upgrading to annual membership

**Response Script:**
"Great choice! Our annual membership offers the best value and commitment to your fitness journey. You'll get all the benefits of membership plus special annual member perks. You can book your upgrade consultation here: https://api.grow.pushpress.com/widget/bookings/annual-upgrade"

**PushPress Workflow:**
- Tag: "Annual Upgrade Interest"
- Book consultation: https://api.grow.pushpress.com/widget/bookings/annual-upgrade
- Follow-up: Upgrade benefits and payment options

### 📋 **Required Information Collection**

#### **For All Prospects:**
- First name
- Email address
- Phone number
- Fitness experience level
- Primary goal

#### **For Drop-ins:**
- Preferred class time
- Date of visit
- Payment preference (online vs. in-person)

#### **For No Sweat Intros:**
- Preferred consultation time
- Primary fitness goals
- Any injuries or limitations
- Best contact method

### 🔄 **PushPress Workflow Setup**

#### **Workflow 1: New to CrossFit Pipeline**
```
Trigger: "New to CrossFit" tag applied
Actions:
1. Schedule No Sweat Intro appointment
2. Send preparation email with what to expect
3. Add to "New Member" nurture sequence
4. Set follow-up reminder for 24 hours before appointment
```

#### **Workflow 2: Experienced Athlete Pipeline**
```
Trigger: "Experienced Athlete" tag applied
Actions:
1. Send class schedule and program information
2. Offer drop-in booking or program consultation
3. Add to "Experienced Athlete" nurture sequence
4. Set follow-up reminder for 3 days
```

#### **Workflow 3: Drop-in Pipeline**
```
Trigger: Drop-in booking or "Local Prospect" tag
Actions:
1. Send class schedule and waiver information
2. Provide payment options (online link or in-person)
3. Send confirmation and preparation details
4. Set follow-up reminder for day after visit
```

#### **Workflow 4: Out-of-Town Guest Pipeline**
```
Trigger: "Out-of-Town Guest" tag applied
Actions:
1. Send online payment link and class schedule
2. Provide local recommendations (restaurants, hotels)
3. Send confirmation and preparation details
4. Set follow-up reminder for day after visit
```

### 🎙️ **Updated Bot Training Data**

#### **Fred (Voice AI) - Routing Questions:**
- "Are you brand new to CrossFit, or have you trained before?"
- "Are you local to Alexandria, or visiting from out of town?"
- "Are you looking to try a class, or are you interested in joining our community?"

#### **Tommy (Conversation Bot) - Detailed Routing:**
- "What's your fitness background - are you new to working out or do you have experience?"
- "Are you local to the area, or are you visiting?"
- "What's your main goal - trying out a class, joining our community, or something specific?"

### 📱 **SMS Bot Routing:**
- Quick questions about classes → Send class schedule
- Drop-in inquiries → Send booking link and instructions
- New member questions → Route to No Sweat Intro booking

### 📲 **Social Media Bot Routing:**
- Program questions → Route to Tommy for detailed discussion
- Class schedule requests → Send schedule and drop-in info
- Community questions → Engage with Trident story and values

### ✅ **Success Metrics**

#### **Routing Accuracy:**
- 90%+ of prospects routed to appropriate experience
- 80%+ of No Sweat Intros convert to members
- 70%+ of drop-ins return for additional visits

#### **Process Efficiency:**
- Under 2 minutes to determine routing
- 95%+ of prospects receive appropriate follow-up
- 100% of prospects sign required waivers

### 🎯 **Implementation Checklist**

#### **Phase 1: Bot Training Updates**
- [ ] Update Fred's routing questions
- [ ] Update Tommy's detailed discovery process
- [ ] Update SMS bot quick responses
- [ ] Update social media bot routing logic

#### **Phase 2: PushPress Workflow Setup**
- [ ] Create "New to CrossFit" workflow
- [ ] Create "Experienced Athlete" workflow
- [ ] Create "Drop-in" workflow
- [ ] Create "Out-of-Town Guest" workflow

#### **Phase 3: Staff Training**
- [ ] Train staff on new routing system
- [ ] Update front desk procedures
- [ ] Create coach handoff protocols
- [ ] Test all routing scenarios

#### **Phase 4: Testing & Optimization**
- [ ] Test all routing paths
- [ ] Monitor routing accuracy
- [ ] Optimize based on results
- [ ] Refine workflows as needed

### 🚀 **Expected Results**

With this smart routing system:
- **New members** get proper onboarding through No Sweat Intros
- **Experienced athletes** get fast-tracked to appropriate programs
- **Drop-ins** have smooth, clear processes
- **Out-of-town guests** get professional, welcoming experience
- **Staff** have clear procedures for every scenario
- **Conversion rates** improve through appropriate routing

This system ensures every prospect gets the right introduction to Trident Athletics based on their experience level and goals, leading to higher satisfaction and better conversion rates!
