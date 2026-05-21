# Instagram User Analytics

## 📊 Project Overview

SQL-based analysis of Instagram user data to provide actionable insights for marketing campaigns and investor metrics. This project demonstrates practical application of SQL queries to solve real-world business problems in social media analytics.

## 🎯 Business Impact

**For Marketing Team:**
- Identify loyal users for reward programs
- Target inactive users for re-engagement campaigns  
- Optimize hashtag strategies and ad campaign timing
- Determine contest winners based on engagement metrics

**For Investors:**
- Measure user engagement and platform activity
- Detect potential bot accounts and fake users
- Assess platform health through key metrics

## 🛠️ Tech Stack

- **MySQL Workbench** - Database management and query execution
- **SQL** - Data analysis and insights extraction

## 📁 Repository Contents

- `Presentation.pdf` - Complete analysis with SQL queries, results, and insights
- `README.md` - Project documentation

## 📈 Key Results

### Marketing Analysis Results:
- **Loyal Users**: Identified 5 earliest users for reward program eligibility
- **Inactive Users**: Found 26 out of 100 users (26%) have never posted a photo
- **Contest Winner**: Zack_Kemmer93 (user_id: 52) won with 48 likes on photo_id 145
- **Popular Hashtags**: Identified top 5 most commonly used hashtags for brand partnerships
- **Ad Campaign Timing**: Thursday and Sunday (especially 16th of month) show highest user registration

### Investor Metrics Results:
- **User Engagement**: Calculated average posts per user and photo-to-user ratio
- **Bot Detection**: Identified suspicious accounts that liked every single photo, indicating automated activity

## 💡 Business Impact
- **26% inactive user base** presents re-engagement opportunity
- **Optimal ad timing** identified for maximum reach
- **Bot detection system** helps maintain platform integrity
- **Hashtag insights** enable strategic brand partnerships

## 🔍 Key SQL Queries

1. **Loyal Users** — `SELECT username FROM users ORDER BY created_at ASC LIMIT 5` — identifies the 5 earliest registered users for a loyalty reward program
2. **Inactive Users** — Users who have never posted (`LEFT JOIN photos ... WHERE photos.id IS NULL`) — 26% of users flagged for re-engagement campaign
3. **Top Hashtags** — Count tag frequency across all photos using `GROUP BY tag_name ORDER BY COUNT(*) DESC LIMIT 5`
4. **Contest Winner** — Identify photo with the most likes using a subquery on the `likes` table
5. **Bot Detection** — Users who have liked every single photo (`HAVING COUNT(*) = (SELECT COUNT(*) FROM photos)`) — flags suspicious automated accounts

## 👤 Author

**Sakhi Patel**  
📧 sakhipatel20@gmail.com

## 🎓 Course Context

Undergraduate SQL analytics project demonstrating query techniques for business intelligence and social media analytics. PDEU, AY 2024–2025.
