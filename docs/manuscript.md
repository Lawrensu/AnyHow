# "Eat Where?" Detailed Overview

This document defines the initial scope of **Eat Where?** before any methodology, system design, or implementation work begins.

The purpose is to clearly understand what problem the startup is trying to solve, what kind of product it is, who it is for, what is inside the current scope, and what should intentionally remain outside the scope as of now.

This document should be treated as the foundation for later documents. If the scope is unclear, the methodology, system design, and implementation will inherit that ambiguity.

---

## 2. Startup Thesis

**Eat Where?** is a food decision platform focused on helping people decide where to eat, especially when multiple people are involved and preferences conflict.

The startup is not primarily trying to solve restaurant discovery. Existing platforms (listed below) already help users find restaurants, reviews, ratings, opening hours, photos, delivery options, and directions:

- Google Maps
- GrabFood
- Waze

The stronger issue here is decision-making.

People often have enough options, but still struggle to choose because each person may have different cravings, budgets, distance preferences, dietary needs, and expectations. In group situations (especially in the context of university), this becomes harder because everyone wants a say, but no one wants to be blamed if the final choice is bad.

Therefore, the startup thesis is:

> Eat Where? helps individuals and groups make food decisions by turning scattered preferences into a clearer, fairer, and more explainable recommendation.

---

## 3. Problem Statement

People often struggle to decide where to eat.

- For individuals, the problem usually starts with uncertainty around craving, cuisine, price, distance, ratings, convenience, or mood.

- For groups, the problem becomes more complex because each person may value different things. One person may want something cheap, another may want something nearby, another may want a specific cuisine, and another may reject certain food entirely.

The decision process can become slow, repetitive, socially uncomfortable, or arbitrary The core problem is not a lack of food options but rather the lack of a structured decision process that fairly combines preferences and helps people reach a final choice.

---

## 4. Problem Context

### 4.1 Individual Context

An individual may struggle because they do not know what they want, have too many choices, or do not want to regret the choice later.

Typical individual decision process:

1. Think about craving or cuisine.
2. Search nearby places.
3. Compare ratings, distance, price, and photos.
4. Keep switching between options.
5. Eventually choose based on convenience, habit, or impulse.

### 4.2 Group Context

A group may struggle because preferences conflict.

Common conflicts include:

1. Cheap versus expensive.
2. Nearby versus better quality.
3. Familiar versus new.
4. Spicy versus mild.
5. Fast versus sit-down.
6. Halal versus non-halal.
7. Healthy versus comfort food.
8. Majority preference versus minority restriction.

In a group, the decision is not only functional. It is social.

A poor choice can create blame, dominant person may decide too often, quiet members may compromise without saying anything. The group may waste time because no one wants to take responsibility.

This makes the group decision problem more valuable and more specific than general restaurant recommendation.

---

## 5. Target Users

### 5.1 Initial Target User

The initial target user is:

> University students deciding where to eat alone or with friends. (I heavily experience this problem a little too often)

This target is chosen because university students often eat in groups, have budget constraints, move around a campus or nearby city area, and make frequent food decisions.


### 5.2 Secondary Users

Possible secondary users include:

1. Office workers deciding lunch as a team.
2. Friend groups planning casual meals.
3. Couples deciding where to eat.
4. Tourists looking for food in an unfamiliar area.
5. Families choosing restaurants together.

These are not the initial priority unless the startup later decides to expand beyond the first target segment. Then, features related to those target users will eventually be considered and thought of.

---

## 6. Product Positioning

Eat Where? should be positioned as a decision layer, not merely a restaurant listing platform as existing food and map platforms are useful for discovery, but they usually leave the final decision to the user or group.

Eat Where? should focus on:

1. Collecting user preferences.
2. Identifying constraints.
3. Comparing options.
4. Reducing disagreement.
5. Producing a final recommendation.
6. Explaining why that recommendation makes sense.

The positioning statement is:

> Eat Where? is a food decision assistant that helps people and groups fairly decide where to eat by combining preferences, constraints, and restaurant data into an explainable recommendation.

---

## 7. Scope Boundary

### 7.1 In Scope

The current scope includes:

1. Understanding how people decide where to eat.
2. Supporting individual and group food decision sessions.
3. Collecting basic food preferences and constraints.
4. Generating restaurant or food-place candidates.
5. Allowing users to compare, reject, vote, or rank options.
6. Producing a final recommendation.
7. Explaining the reason behind the recommendation.
8. Keeping the first implementation simple enough to validate the core decision problem.

### 7.2 Out of Scope

The current scope does not include:

1. Food delivery ordering.
2. Payment processing.
3. Restaurant reservation handling.
4. Restaurant owner dashboards.
5. Advertising systems.
6. Loyalty points.
7. Full social media features.
8. Complex long-term taste profiling.
9. Advanced AI personalization.
10. Building a complete restaurant database from scratch.

These features may become relevant later, but they should not be included in the first version unless they directly support the core decision problem.

---

## 8. Core Product Flow

The expected core flow is:

1. A user starts a food decision session.
2. The user chooses whether the session is individual or group-based.
3. The user provides basic context such as location, budget, craving, cuisine, and constraints.
4. For group sessions, other participants join through an invite link.
5. Each participant submits preferences, constraints, or votes.
6. The system generates possible places to eat.
7. The system filters unacceptable options.
8. The system ranks remaining options.
9. The system recommends one or more final choices.
10. The system explains why the recommendation was made.

The flow should remain simple. The product should reduce decision fatigue, not introduce another complicated decision process.

---

## 9. Core Value Proposition

The value proposition is:

> Eat Where? reduces the time, friction, and uncertainty involved in deciding where to eat.

For individuals, it helps narrow choices.

For groups, it helps create a fair decision process.

The product is valuable if it can help users answer:

> “Where should we eat, and why does this choice make sense for us?”

---

## 10. Early Product Principles

### 10.1 Decision First

The product should prioritize helping users reach a decision, not endlessly browse options.

### 10.2 Explainability

The system should explain recommendations clearly. Users should understand why a place was suggested.

### 10.3 Low Friction

Users should not be forced through unnecessary setup just to decide where to eat.

### 10.4 Fairness in Groups

The system should avoid simply letting the loudest person or majority preference dominate every decision.

### 10.5 Simplicity Before Complexity

The first version should solve the smallest meaningful version of the problem.

### 10.6 Separation of Concerns

The frontend should render the experience. The backend should enforce decision logic. The database should store data. External APIs should provide restaurant or location data.

---

## 11. Key Assumptions

The current assumptions are:

1. People experience meaningful friction when deciding where to eat.
2. Group food decisions are more painful than individual food decisions.
3. University students are a suitable first target segment.
4. Users are willing to provide lightweight preferences if the result is useful.
5. Users prefer a clear recommendation over a long list of options.
6. Group users value fairness and blame reduction.
7. Existing platforms do not fully solve group consensus.
8. External restaurant data can be integrated later instead of built manually from scratch.

These assumptions are not facts. They must eventually be tested.

---

## 12. Open Questions

The following questions remain unresolved:

1. Should the first version focus on individuals, groups, or both?
2. Should the first target users be university students specifically?
3. Should the product recommend restaurants, dishes, cuisines, or all three?
4. Should users vote on generated options or provide preferences first?
5. Should the system produce one final answer or a ranked shortlist?
6. How much user input is acceptable before the process feels too slow?
7. Should anonymous group participation be allowed?
8. What data source should be used for restaurant information?
9. Should traffic and travel time be included in the first version?
10. What makes a recommendation feel fair to the group?

These questions should be answered gradually through methodology, testing, and product reasoning.

---

## 13. Current Working Definition of Success

Eat Where? succeeds at the scope level if it can help users move from uncertainty to a justified food decision.

A successful product session should result in:

1. Less confusion.
2. Less repeated discussion.
3. A clearer final choice.
4. A recommendation that users understand.
5. A decision that feels acceptable to the group.

The first version does not need to be perfect. It needs to prove that structured decision-making creates value in food selection.

---
