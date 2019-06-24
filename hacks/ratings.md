---
hackname: ratings
quicksummary: Simple system to allow P2P ratings
resource: true
archived: false
categories: [hack]
---

# Ratings

Short description -> Allow users to rate eachothers

## I'm on mini bacation for pitching

- Therefore someone else (probably Nico or Tanya) will have to present, or find someone to read this document out loud :D it has everything

## Who's Participating?

- [Marko Kostovski](/hackdays/whoami/marko)
- [Branko Popovic](/hackdays/whoami/branko) -> even tho he will not be with us in person, he thinks that rating system is great idea, and he is willing to contribute
- Android dev would be great
- We NEED at least one more person to handle backend
- Anyone else who wants to work, we will have job for design, wording, project itself :D

## Problem 1

Nico wants to buy a used iPhone 7 for 150 CHF, he has found the item on tutti.ch and he is ready to contact the seller. However, even tho the item looks great, seller is living in opposite part of the Switzerland and they cannot meet in person. Nico is not sure is seller trustworthy. He is hesitating to buy an item that is not as cheap - and the clock is ticking [dramatic music playing in background]

## Problem 2

- [Real example](/hackdays/assets/images/selda-story.png) (click)

## Solution

It is our responsibility to provide system to make our users feel more secure when they are buying or selling items. By checking out Serbian equivalents of tutti.ch (they are pretty good actually) most of them have rating system and they are accepted by our users as standard for measuring trustworthiness.

## Challenges

- If implemented incorrectly, rating system can cause damage because we will always have people trying to exploit system. (thank you Nunzio for giving me insight)
- In order to implement rating system properly, we would need messaging system as well (2 in 1, how awesome is that :D)

## Requirments (stolen from Serbian websites, and modified a bit) so that we know can one user rate another

- Users are sending messages one to another (two-way is mandatory), it serves as a proof that there has been interaction between 2 users (this is probably going to be developed if we get extra time for project)
- Seller has marked his item as “SOLD”
- Ratting cannot happen more then 5 days after the item has been marked as “SOLD”
- You cannot rate user more then once every 2 weeks no matter how much items have you traded

After that user rate :+1: or :-1: along with the description and all ratings are visible from user profile.
