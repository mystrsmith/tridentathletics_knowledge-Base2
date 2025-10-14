# Trident Athletics Booking Links Reference
## Complete PushPress Booking Widget URLs

### 🎯 **Primary Booking Links**

#### **1. No Sweat Intro (New Members)**
**URL:** https://api.grow.pushpress.com/widget/bookings/trident-bookings
**Purpose:** Free 30-minute consultation for new members
**Target Audience:** New to fitness, new to CrossFit
**Use Cases:**
- First-time visitors
- Complete beginners
- People new to CrossFit
- Anyone wanting to learn about Trident

#### **2. Annual Upgrade (Current Members)**
**URL:** https://api.grow.pushpress.com/widget/bookings/annual-upgrade
**Purpose:** Membership upgrade consultation
**Target Audience:** Current monthly members
**Use Cases:**
- Members wanting to upgrade to annual membership
- Cost savings inquiries
- Commitment level discussions

#### **3. Dad Bod Strong Program**
**URL:** https://api.grow.pushpress.com/widget/bookings/dad-bod
**Purpose:** 6-month transformation program consultation
**Target Audience:** Men 38-55
**Use Cases:**
- Men interested in transformation programs
- Age-specific fitness goals
- Comprehensive lifestyle change

### 🤖 **Bot Integration Instructions**

#### **Fred (Voice AI Bot) Usage:**
```
For No Sweat Intro: "You can book your No Sweat Intro at tridentathleticsva.com or I can send you the link."

For Dad Bod Strong: "Perfect for your goals! I can send you the Dad Bod Strong consultation link."

For Annual Upgrade: "Great choice! I'll get you connected with our upgrade consultation."
```

#### **Tommy (Conversation Bot) Usage:**
```
For No Sweat Intro: "You can book it right here: https://api.grow.pushpress.com/widget/bookings/trident-bookings"

For Dad Bod Strong: "You can book your consultation here: https://api.grow.pushpress.com/widget/bookings/dad-bod"

For Annual Upgrade: "You can book your upgrade consultation here: https://api.grow.pushpress.com/widget/bookings/annual-upgrade"
```

#### **SMS Bot Usage:**
```
Quick responses with direct links:
"No Sweat Intro: [link]"
"Dad Bod Strong: [link]"  
"Annual Upgrade: [link]"
```

### 📋 **Routing Decision Tree**

```
PROSPECT CONTACTS TRIDENT
         ↓
    WHAT'S THEIR SITUATION?
    ┌─────────────────────────┐
    │  NEW TO FITNESS/CROSSFIT│ → trident-bookings
    │  CURRENT MEMBER         │ → annual-upgrade
    │  MAN 38-55 TRANSFORM    │ → dad-bod
    │  EXPERIENCED ATHLETE    │ → Drop-in process
    │  OUT-OF-TOWN GUEST      │ → Drop-in process
    └─────────────────────────┘
```

### 🏷️ **PushPress Tags for Automation**

#### **Auto-Tagging Rules:**
- **"New to CrossFit"** → Use trident-bookings link
- **"Annual Upgrade"** → Use annual-upgrade link
- **"Dad Bod Strong"** → Use dad-bod link
- **"Experienced Athlete"** → Drop-in process
- **"Out-of-Town Guest"** → Drop-in process

### 📧 **Email Template Integration**

#### **No Sweat Intro Email:**
```
Subject: Your No Sweat Intro is Scheduled!

Hi [Name],

Your No Sweat Intro consultation is confirmed for [Date] at [Time].

Book additional sessions: https://api.grow.pushpress.com/widget/bookings/trident-bookings
```

#### **Dad Bod Strong Email:**
```
Subject: Dad Bod Strong Consultation Scheduled!

Hi [Name],

Your Dad Bod Strong consultation is confirmed for [Date] at [Time].

Book additional sessions: https://api.grow.pushpress.com/widget/bookings/dad-bod
```

#### **Annual Upgrade Email:**
```
Subject: Annual Membership Upgrade Consultation

Hi [Name],

Your annual upgrade consultation is confirmed for [Date] at [Time].

Book additional sessions: https://api.grow.pushpress.com/widget/bookings/annual-upgrade
```

### 🔄 **Workflow Integration**

#### **Workflow Triggers:**
1. **Contact books No Sweat Intro** → Tag "No Sweat Intro Booked"
2. **Contact books Dad Bod Strong** → Tag "Dad Bod Strong Booked"
3. **Contact books Annual Upgrade** → Tag "Annual Upgrade Booked"

#### **Follow-up Sequences:**
- **No Sweat Intro:** 5-email sequence over 14 days
- **Dad Bod Strong:** 7-email sequence over 21 days
- **Annual Upgrade:** 3-email sequence over 7 days

### 📱 **Website Integration**

#### **Embed Codes:**
```html
<!-- No Sweat Intro Widget -->
<iframe src="https://api.grow.pushpress.com/widget/bookings/trident-bookings" 
        width="100%" height="600" frameborder="0"></iframe>

<!-- Dad Bod Strong Widget -->
<iframe src="https://api.grow.pushpress.com/widget/bookings/dad-bod" 
        width="100%" height="600" frameborder="0"></iframe>

<!-- Annual Upgrade Widget -->
<iframe src="https://api.grow.pushpress.com/widget/bookings/annual-upgrade" 
        width="100%" height="600" frameborder="0"></iframe>
```

### 🎯 **Success Metrics**

#### **Booking Conversion Rates:**
- **No Sweat Intro:** Target 60%+ conversion to members
- **Dad Bod Strong:** Target 80%+ completion rate
- **Annual Upgrade:** Target 70%+ upgrade rate

#### **Performance Tracking:**
- **Link clicks per bot interaction**
- **Booking completion rates**
- **Follow-up sequence engagement**
- **Revenue per booking type**

### 🚀 **Implementation Checklist**

#### **Bot Training:**
- [ ] Update Fred with booking link references
- [ ] Update Tommy with direct booking links
- [ ] Update SMS bot with quick link responses
- [ ] Update social media bot with program-specific links

#### **Website Integration:**
- [ ] Embed booking widgets on website
- [ ] Test mobile responsiveness
- [ ] Verify payment processing
- [ ] Test waiver integration

#### **Workflow Setup:**
- [ ] Create auto-tagging rules
- [ ] Set up follow-up sequences
- [ ] Configure email templates
- [ ] Test automation triggers

#### **Staff Training:**
- [ ] Train staff on booking link usage
- [ ] Create quick reference guide
- [ ] Test booking processes
- [ ] Monitor performance metrics

### 💡 **Pro Tips**

#### **Link Usage Best Practices:**
1. **Always provide context** before sharing links
2. **Explain what to expect** in the consultation
3. **Follow up** after sharing links
4. **Track performance** of each booking type
5. **Optimize** based on conversion rates

#### **Common Scenarios:**
- **Unsure which link:** Start with trident-bookings (No Sweat Intro)
- **Multiple interests:** Book separate consultations for each program
- **Urgent requests:** Provide direct links with immediate follow-up
- **Complex needs:** Combine multiple booking types as needed

This reference ensures consistent use of the correct booking links across all AI bots and touchpoints, leading to better conversion rates and member experience!
