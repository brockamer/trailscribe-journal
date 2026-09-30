---
title: "One prompt, three models: a copy A/B test"
date: 2026-09-30T15:41:46.000Z
excerpt: "The same TrailScribe prompt, run through the model that writes these posts today and two newer ones. Test inputs, not a trip."
tags: [trailscribe, experiment]
---
**This is a test post, not a trip.** The places and weather below are test inputs. I wanted to see how much the model that writes TrailScribe's copy matters, so I ran the Worker's own narrative code, unmodified apart from one setting described below, against three models, four inputs and four samples each, 48 pieces of copy in all. Below is **sample 1 of each model for each input**, chosen by rule before reading any of them, not picked for looks.

The three models:

- **A. Claude Sonnet 4.6**, what writes the posts today.
- **B. Claude Opus 5.5.**
- **C. Claude Sonnet 5.5.**

## The numbers

| | A · Sonnet 4.6 | B · Opus 5.5 | C · Sonnet 5.5 |
|---|---|---|---|
| Haiku is 5/7/5 (approximate counter) | 15 of 16 | 16 of 16 | 16 of 16 |
| No-caption, clear sky: names a time of day the data does not contain | **4 of 4** | 0 of 4 | 0 of 4 |
| Average body length (limit 500) | 376 characters | 297 | 223 |
| Cost per post, narrative call only | $0.0033 | $0.0127 | $0.0076 |

Two caveats before you read the copy. First, four samples per cell is a small test, and the counts above are illustrations, not statistics. Second, models B and C think before they answer, and that hidden thinking counts against the Worker's 600-token limit. I raised the limit to 2,000 for B and C only. At the real limit of 600, Opus 5.5 failed 4 of 32 calls with unparseable output. The one failure I captured in full had been cut off mid-string when it hit the limit. So switching models would also mean raising that limit.

## 1. A terse caption

Inputs:  
Note: test from bedroom  
Location: Malibu, California (34.027, -118.836)  
Weather: 69°F, 10mph, clear

**A · Sonnet 4.6 (what production runs today)**

> **Still Morning in Malibu**
>
> warm air off the sea  
> curtains lift and fall again  
> nothing moves out there
>
> Sitting still. The window faces west and the light is doing something quiet with the walls. Sixty-nine degrees feels exactly right — not a temperature you notice, which is the point. Wind out of the west at ten, just enough to remind you the Pacific is close. No notes to speak of. Sometimes the test is the entry.

**B · Opus 5.5**

> **Test Entry from the Bedroom, Malibu**
>
> A test from bedroom  
> clear Malibu sky outside  
> warm breeze at the glass
>
> Test from the bedroom. No trail today, just making sure the notes come through. Outside it's 69°F and clear over Malibu, with a 10 mph breeze. Good conditions to file away for when the real entries start.

**C · Sonnet 5.5**

> **Test Entry from a Bedroom Basecamp**
>
> Bedroom window light  
> a test of the signal, sent  
> Malibu breeze stirs
>
> A test entry, logged indoors from a bedroom in Malibu. Outside it is 69°F with a light 10 mph wind and clear skies. No trail, no miles, no summit today. This is just a check that the journal works.

## 2. A descriptive caption

Inputs:  
Note: Made the saddle at last. Wind is picking up and there is still snow on the north side. Legs are done.  
Location: Inyo County, California (37.168, -118.589)  
Weather: 38°F, 22mph, partly cloudy

**A · Sonnet 4.6 (what production runs today)**

> **Saddle Gained, Wind at the Ridge**
>
> Cold wind finds the gap  
> north slopes still hold winter white  
> legs have nothing left
>
> Made the saddle after a long grind. Wind hits hard up here, steady and cold, cutting right through the shell. The north-facing slope is still patched with snow — not surprising at this elevation in the Sierra. Legs are cooked. Standing here long enough to take it in, then I'll need to decide whether to push on or find a sheltered spot below the ridgeline to rest. The sky is holding for now, but that wind has an edge to it.

**B · Opus 5.5**

> **Wind at the Saddle, Snow to the North**
>
> Wind combs the high pass  
> Snow clings to the northern slope  
> My legs have gone still
>
> Made the saddle at last. The wind is picking up, blowing around 22 mph, and at 38°F it cuts right through. There's still snow on the north side, holding on where the sun doesn't reach. Clouds are drifting over, the light coming and going. My legs are done, with nothing left in them. Time to pull on another layer, find a spot out of the wind if there is one, and sit with having made it up here.

**C · Sonnet 5.5**

> **Saddle, Wind, and Spent Legs**
>
> Saddle at long last  
> Snow still clings to the north side  
> Wind rises, legs done
>
> Made the saddle at last. It's 38°F up here, and the wind has picked up to around 22 mph under partly cloudy skies. Snow still lingers on the north side. My legs are done, so I'm going to stand here a while and catch my breath before deciding anything else.

## 3. No caption, clear sky

Inputs:  
Location: Malibu, California (34.027, -118.836)  
Weather: 69°F, 10mph, clear

**A · Sonnet 4.6 (what production runs today)**

> **Clear Afternoon Along the Malibu Coast**
>
> Salt air holds steady  
> ten miles of wind off the sea  
> clear light, sixty-nine
>
> The coordinates place the traveller near the Malibu coastline, where the Pacific sets the baseline for everything — temperature, humidity, the low persistent push of a ten-mile-per-hour onshore breeze. At 69°F under a clear sky, the marine layer has pulled back. Shadows are sharp. The horizon is unobstructed. Conditions are neither harsh nor remarkable; this is the coast on a cooperative afternoon.

**B · Opus 5.5**

> **Clear Sky over the Malibu Coast**
>
> Sixty-nine degrees  
> clear sky over Malibu  
> a ten mile breeze blows
>
> Position logged at 34.027, -118.836, along the Malibu stretch of the Southern California coast, where the Santa Monica Mountains meet the Pacific. Conditions are clear, with the air at 69°F and a 10 mph wind moving across the area. The sky is unobstructed and the temperature is mild.

**C · Sonnet 5.5**

> **Clear Air Over Malibu, Light Wind**
>
> Malibu, clear sky  
> sixty-nine degrees, light wind  
> coast lies open, bright
>
> Malibu, California, at roughly 34.027 N, 118.836 W, near the Pacific coast. The sky is clear, the air is 69°F, and wind runs about 10 mph. Mild, open conditions with nothing in the sky.

## 4. No caption, fog

Inputs:  
Location: Mendocino, California (39.305, -123.799)  
Weather: 52°F, 6mph, fog

**A · Sonnet 4.6 (what production runs today)**

> **Fog Hold Over Mendocino Headlands**
>
> coastal fog holds still  
> salt air at fifty-two degrees  
> the bluff edge goes gray
>
> A position on the Mendocino coast, latitude 39.3, longitude -123.8. Fog sits over the headlands at 52°F, wind negligible at 6 mph from the west. Visibility is reduced; the Pacific margin dissolves into gray before any horizon resolves. The temperature is steady, typical of a marine layer that has not yet lifted. No sun angle is discernible from this report.

**B · Opus 5.5**

> **Fog Over Mendocino**
>
> Mendocino fog  
> fifty-two degrees, light wind  
> headlands fade to gray
>
> Mendocino, California, on the Pacific coast of the northern part of the state, at 39.305, -123.799. Fog holds over the position. The air sits at 52°F with a light wind of about 6 mph, not enough to clear the fog. Visibility is reduced, and the coastline is muted under the gray.

**C · Sonnet 5.5**

> **Fog Along the Mendocino Coast**
>
> Fog on the headlands  
> Fifty-two degrees, light wind  
> Coast holds its gray breath
>
> Position near Mendocino, California (39.305, -123.799). The air sits at 52°F with a 6 mph wind, and fog is reported. Conditions are cool and damp, with only light air movement.

## What I noticed

- **A adds details the data does not contain.** With no caption, all four of its clear-sky posts say "afternoon". Across those four it also adds an onshore breeze, chaparral-covered slopes and a marine layer that "has pulled back". The system prompt says not to invent specifics. On the terse caption it wrote "Still Morning in Malibu" with a west-facing window.
- **B and C stay inside the data.** They are plainer. C is the plainest and shortest, and B sits between.
- **This is the same kind of mismatch as a night-time image under an "evening" post.** When a bare post asserts a time of day, the image and the words can disagree.
- **Whether A's richer prose is worth the invention is a taste call.** That is why the candidates are here for you to read.

*Images were not compared. The bare-caption image is drawn from the narrative, so a different model does change it, but rendering one needs the image API key, which this test did not have.*
