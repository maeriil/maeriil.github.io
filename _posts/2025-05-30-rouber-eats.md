---
title: "Rouber-Eats Features"
date: 2025-05-30
categories: [portfolio, casual, food, ui, icons]
tags: [game, delivery]
---
### Overview

Rouber eats was one of the major game I was working on as a solo dev. The premise of the game is simple; Select orders to deliver, go to the restaurant and pickup the order; and finally deliver the food to the destination. Despite this, this game was abandoned because I struggled a lot with the game designs. There were few problems from the design perspective which I couldn't solve. They were
1. Delivering after few times was becoming boring
2. The money that we earned from each delivery was a bit pointless.
3. Not much else to do in the game.

### Features
#### Icons and UI
I really wanted to focus a bit more on the UI side of things for this project. Looking back, I think that was a mistake and rather should be focused on the later half of the project, but as they say, learning by doing. Neverthless, here are some cool UI I made during this time.

This was the icons I created from Figma for the game
![Icon pack image](/assets/rouber-eats-icon-pack.png)

This was the victory screen's reward screen I created for the game. The bars are animated.
![Reward screen](/assets/rouber-eats-reward-screen.png)

This was the phone screen for the game. Phone is where every app would be stored, as well as how we would view the orders, and accept them, just like in real life.
![Phone screen](/assets/rouber-eats-phone.png)

This was the inventory screen
![Inventory screen](/assets/rouber-eats-2.png)

One of the major features in the game is the Dialogue screen. Visually they look like this
<iframe width="100%" height="400"
  src="https://www.youtube.com/embed/URNzN36H1gY"
  title="Dialogue demo video"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen>
</iframe>

The creation of this dialogue was also a lot simple. In fact it would support things like yielding, goto, choices. An example snippet would look like. (Unfortunately markdown doesn't seem to support Luau syntax :sob:)
```luau
CHOICE {
        text = `I spoke with the owner and they told me I can keep it!`,
        RESPONSE {
            text = `Did they really say that?`,
            CHOICE {
                text = `Yes. I am sure`,
                IF(select_choice_to_steal()) {
                    success = {
                        RESPONSE {
                            text = `Fair enough, here is your order! Have a great day!`,
                        },
                    },
                    failure = {
                        RESPONSE {
                            text = function()
                                return `No you do not! {error_msg_handling}`
                            end,
                            --// The order is still marked as in process, so we should force them to deliver it
                            GOTO {
                                key = "choice_goto",
                            },
                        },
                    },
                },
            },
            CHOICE {
                text = `No, I would like to rethink my decision...`,
                GOTO {
                    key = "choice_goto",
                },
            },
        },
    },
```

Here, `select_choice_to_steal` is a yieldable function, which fires to server and awaits feedback from the server.

### Rouber Issues
#### Delivering after few times was becoming boring

This was becoming more and more apparant when I was doing some test runs on the game. After a while it just becomes repetitive. The *[Work at a Pizza Place!](https://www.roblox.com/games/192800/Work-at-a-Pizza-Place)*  does not suffer from this as they have multiple jobs. Which means if a player is bored from just selecting orders, they can change their job to *Cooking*, or *Packaging*, or even *Delivering*. In this game, we don't have those options, rather we only have one, which is to *Delivery*. I felt it didn't really make sense to add multiple other jobs.

In order to "resolve" this issue, I tried adding a mechanism whilst we go pickup the order in Restaurant. When we attempt to pickup an order, we have three options; To deliver the order to the right house, To alter the order, or To steal the order. Delivering meant we just earned some money. Altering meant we could add some toppings to the order, and depending on the destination's npcs's preferences, it could result in more or less money. And finally, stealing the order meant we kept it to ourselves.

This didn't seem to resolve much, and instead introduced new issues. Namely, what would be the point of stealing orders? I tried to introduce pet system, something like, the food we steal turns into pet. However, this didn't work out well and was scrapped. Therefore to this day, this issue wasn't resolved.

#### The money that we earned from each delivery was a bit pointless

Like above, I don't think I fully solved this issue either. It was simply hidden a bit. What I did was introduce a furnishing system to our base, and each base item would use some money to place it on our plot. While it does kinda work, I don't think its correct, as the core loop of the game has nothing to do with money. But in some ways, *Work at a Pizza Place* also doesn't really have money tied to the core game, so perhaps I am going about it the wrong way...

#### Not much else to do in the game

This one is also true, the map isn't complete, and right now, there isn't really whole lot to do with the game. In order to combat this, I introduced a simple progression system. Its working, but its not that satisfying. Before I could fully fix the bugs, I decided to drop the game as I felt a bit lost.


#### Now what?
Perhaps in the near future I will decide to revist this game again. But for now, this was honestly a complete failure. It made me realize that game design in the games is super crucial. This game was really terrible from game design perspective.
- The onboarding was very bad
- the game was not simple to understand
- the game wasn't fun to play constantly

If this game wants to have any chance of success, those three points will need to be fixed first before creating it. Back to the drawing board we go unfortunately..
