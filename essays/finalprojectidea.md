---
layout: essay
type: essay
title: "Party Palooza!"
date: 2023-03-28
labels:
  - Software Engineering
  - Meteor
  - Matchmaking
  - Video Games
---
# Party Palooza!
*Authors: Christopher Pascual, Mark Burgess, Tung Nguyen*
<br />
## Overview
*The Problem*: When playing a team-based multiplayer game like Rainbow 6 Siege, Valorant, or CS:GO, gamers often find themselves missing an extra player and have to resort to the game's matchmaking for one. The problem with this is that you can't choose who that random player is. Oftentimes, players are paired with bad teammates, hackers, trollers, and the like who just make the gaming experience horrible.

*The Solution*: Party Palooza! It's a web-based application meant for gamers to choose other gamers to join their team for an online match. Bygone are the days of hopelessly praying to the RNG gods for a good player.

## Approach
To use Party Palooza, players must create a profile. When creating a profile, they can set their username, pick their favorite games, pick interests, and give a short description of themselves.

Once logged in, players are shown options for different games to ensure that they find players for the specific game they want to play. After that, a wide range of other users' profiles is presented to the user.

Users are given 2 options when searching:
1) Manually look through all the users listed
2) Using the automatic search, which shows another player with similar interests.

Once the user finds a player, they can send them a message. The user can also receive messages from other users.

Admins are able to remove users from the site and are given the authority to add and remove games from their site.

## Case Idea
- New User comes to the landing page, views games listed, creates profile, finds other users, sends them a message
- User comes to the landing page, signs in, adds games to a favorited list, finds teammates
- Admin comes to the landing page, signs in, can add/edit games listed on site
- Users can message each other and view messages from others

## Mockup Page Ideas
- Landing Page
- User Home Page
- Admin Home Page
- Favorite Games Page
- Find Teammates Page
- Edit User Profile
- Popular Games Page
- Add Game Page (admin)
- Edit Games Page (admin)
- Message Page

## Beyond the Basics
- Messaging system
- Random teammate finder based on similar interests
- Blocking system
- Game/Interest filter system
