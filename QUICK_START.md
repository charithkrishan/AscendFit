# 🚀 AscendFit Quick Start Guide

## Installation & Setup

### 1. **Install Dependencies**
```bash
cd ascendfit
npm install
```

### 2. **Start Development Server**

**For Web (Browser)**
```bash
npm run web
```
The app will open at `http://localhost:8081`

**For iOS (Mac only)**
```bash
npm run ios
```

**For Android**
```bash
npm run android
```

---

## 📱 First Time Setup

### 1. **Signup**
- Enter your name
- Select your age (must be 16+)
- Choose your gender
- Enter height (cm) and weight (kg)
- Select your fitness goal:
  - Fat Loss
  - Muscle Gain
  - Strength
  - Endurance

### 2. **Personalized Plan**
After signup, the app automatically generates a personalized weekly workout plan based on your goal.

---

## 🎮 Navigation

The app has 9 main screens accessible via bottom tab navigation:

| Tab | Screen | Purpose |
|-----|--------|---------|
| 🏠 | Home | Daily quest, rank progress, quick access |
| 💪 | Workouts | Select and complete exercises |
| 📚 | Library | Browse all exercises with tutorials |
| 🎮 | Game Mode | Boss battles and competitive matches |
| 📋 | Plan Mode | AI trainer with personalized plans |
| ⚔️ | Clans | Create/join clans and clan wars |
| 📊 | Progress | Track weight, measurements, photos |
| 🏆 | Leaderboard | Global rankings and statistics |
| 👤 | Profile | User stats and settings |

---

## 🎯 Daily Workflow

### **Morning**
1. Open app and check **Home** screen
2. View today's **Daily Quest** (+20 XP)
3. Check your current **Rank** and **XP Progress**

### **Workout Time**
1. Go to **Workouts** tab
2. Select an exercise
3. View instructions and common mistakes
4. Complete the exercise and track reps
5. Mark exercise as complete

### **Evening**
1. Check **Progress** tab
2. Log weight/measurements if needed
3. View **Leaderboard** to see where you rank
4. Check **Clan** activities

---

## 💡 Key Features Explained

### **Rank System**
- **Start**: Rank Z (beginner)
- **Goal**: Reach Rank A (advanced)
- **Beyond A**: Advanced ranks (Iron → Steel → Titan → Apex)
- **Leagues**: Competitive divisions after Apex
- **Progression**: 1000 XP = 1 rank up

### **Daily Quest**
- **Reward**: +20 XP for completing workout
- **Penalty**: -20 XP for skipping
- **Zero XP Trigger**: Activates 2× difficulty penalty quest
- **Streak**: Consecutive days of completion

### **Game Mode**
- **6 Game Types**: Boss battles, 1v1, Co-op, Raids, Clan Wars, World Boss
- **Damage**: Based on reps performed
- **Critical Hits**: Perfect form = 2× damage
- **Combos**: Consecutive hits = damage multiplier

### **Plan Mode**
- **AI Trainer**: Generates personalized weekly plans
- **Progressive Overload**: Reps increase each week
- **Deload Weeks**: Every 4th week for recovery
- **Customizable**: By goal and experience level

### **Clans**
- **Create**: Start your own clan
- **Join**: Find and join existing clans
- **Wars**: Compete against other clans
- **Leaderboard**: Clan rankings and stats

---

## 🎮 Game Mode Tutorial

### **Starting a Battle**
1. Go to **Game Mode** tab
2. Select game type (e.g., Solo Boss Battle)
3. Choose a boss
4. Battle begins!

### **During Battle**
- **ATTACK Button**: Deal normal damage (20-50)
- **CRITICAL Button**: Deal critical damage (50-100, 2× multiplier)
- **Health Bar**: Shows boss remaining HP
- **Your Damage**: Total damage dealt this battle

### **Winning**
- Reduce boss HP to 0
- See "ASCENDA!" victory screen
- Earn XP and loot
- Stats update automatically

---

## 📊 Progress Tracking

### **Weight Tracking**
- Log weight weekly
- Automatic BMI calculation
- Visual weight change indicator
- Historical data graph

### **Body Measurements**
- Chest, Waist, Arms, Legs
- Track muscle growth
- Measure progress over time

### **Progress Photos**
- Take weekly photos (front, side, back)
- Build before/after comparison
- Visual transformation tracking

### **Streaks**
- Current streak: Days of consecutive workouts
- Longest streak: Your personal best
- Total workouts: Lifetime count

---

## 🏆 Leaderboard

### **Global Rankings**
- Top 10 players displayed
- Sorted by total XP
- Shows rank, level, and streak
- Real-time updates

### **Your Position**
- See your rank number
- Compare with top players
- Track progress over time

---

## ⚙️ Settings & Profile

### **Profile Screen**
- View personal stats
- Age, height, weight, goal
- Current rank and level
- Total XP and streak
- Reps per set

### **Settings**
- Notifications
- Appearance (Dark/Light)
- Privacy settings
- About AscendFit
- Logout

---

## 🎨 UI Tips

### **Colors**
- **Cyan (#00d9ff)**: Primary accent, interactive elements
- **Dark (#0a0e27)**: Background
- **Red (#ff6464)**: Danger, penalties, boss battles
- **Green (#00ff88)**: Success, wins

### **Animations**
- Smooth transitions between screens
- Pulsing XP bars during loading
- Glowing rank cards
- Damage pop-ups during battles

---

## 🐛 Troubleshooting

### **App Won't Start**
```bash
# Clear cache and reinstall
npm run reset-project
npm install
npm run web
```

### **Port Already in Use**
```bash
# Use different port
npm run web -- --port 8082
```

### **Build Errors**
```bash
# Clear node_modules and reinstall
rm -rf node_modules
npm install
```

---

## 📱 Mobile Testing

### **iOS (Mac)**
```bash
npm run ios
```

### **Android**
```bash
npm run android
```

### **Web (Any Device)**
```bash
npm run web
# Then open http://localhost:8081 on any device
```

---

## 🎯 Goals & Objectives

### **Week 1**
- Complete 5 daily quests
- Reach rank Y
- Try all game modes
- Join a clan

### **Week 2-4**
- Maintain 7-day streak
- Reach rank X
- Participate in clan war
- Log progress photos

### **Month 1**
- Reach rank M
- 20+ total workouts
- Join leaderboard top 100
- Unlock first badge

### **Long Term**
- Reach rank A
- Advance to Iron rank
- Climb competitive leagues
- Become clan leader

---

## 🎉 Tips for Success

1. **Consistency**: Complete daily quests for streak bonuses
2. **Form Over Speed**: Focus on proper form for critical hits
3. **Progressive Overload**: Increase reps as you rank up
4. **Join a Clan**: Compete with friends and earn clan XP
5. **Track Progress**: Log measurements and photos weekly
6. **Use Plan Mode**: Follow AI trainer for optimal progression
7. **Compete**: Challenge others in Game Mode
8. **Rest**: Take deload weeks for recovery

---

## 📞 Support

For issues or questions:
- Check the **Library** for exercise tutorials
- Review **Profile** for stats explanation
- Visit **Help** section in settings

---

## 🚀 Ready to Ascend?

You're all set! Start your fitness journey in AscendFit today.

**Remember**: Every rep counts. Every quest matters. Rise to the top!

**ASCENDA!** 💪✨
