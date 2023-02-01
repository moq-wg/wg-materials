# IETF MoQ Working Group Interim 23-01 Meeting Agenda

* [Meeting arrangements](https://github.com/moq-wg/wg-materials/blob/master/interim-23-01/arrangements.md)
* [Warp Draft](https://kixelated.github.io/warp-draft/draft-lcurley-warp.html)
* [Issues List](https://github.com/kixelated/warp-draft/issues)
* [Open PRs](https://github.com/kixelated/warp-draft/pulls)

## Covid Policy

As of January 1, 2023, Meta no longer requires proof of vaccination to enter its
offices.

We're asking in-person attendees to take a rapid test each day and refrain from
coming if they test positive.  Masks are optional in the meeting room.

## Tuesday, January 31:

[Zoom Link](https://fb.zoom.us/j/92637375736)

Passcode: 298220

[MeetEcho Session](https://meetings.conf.meetecho.com/interim/?short=efac8b55-b9aa-491b-abd9-4da9b0579e31) for Blue Sheets/Queue/Chat

[Zulip Chat Link](https://zulip.ietf.org/#narrow/stream/moq)

[Notes](https://notes.ietf.org/notes-ietf-interim-2023-moq-03-moq)

 **9:00 -  9:30: Room and Check-in open**

 **9:30 - 10:00: Kick off**

* Welcome, Introductions
* Scribes, Blue Sheets, NOTE WELL
* Goals for the interim
* [Chair Slides](https://github.com/moq-wg/wg-materials/blob/main/interim-23-01/MoQ%20Interim%2023-01.pdf)

**10:00 -  Lunch: Results of real world experiments & discussion**

Approximately 25 minutes each, split between presentation and dicussion, with a 20 minute break after the third presentation

* [WebTransport frame per stream transport performance](https://github.com/moq-wg/wg-materials/blob/main/interim-23-01/MoQ_Interim_Jan_31_2023.pdf), Bernard Aboba
* [Warp implementation and results](https://urldefense.com/v3/__https://docs.google.com/presentation/d/17lM0oGhpSRwMGCxbUS3PRmn8YgtcW9EKuClMKcM-Ihg/edit?usp=sharing__;!!Bt8RZUm9aw!4HP8i1S8jyWUjt5MxaXW6k3-BVDCf0vtArcXCXi-zZOCRe6G0GoJ03IsdafV95LyXfSMU_rIs2ln0w9OT0rP$), Ali Begen
* [Warp in QUICR](https://github.com/moq-wg/wg-materials/blob/main/interim-23-01/Warp%20in%20QUICR%2C%20Datagrams%20and%20Congestion.pdf), Datagrams and Congestion, Christian Huitema
* [DTP](https://github.com/moq-wg/wg-materials/blob/main/interim-23-01/DTP_MoQ_interim.pdf), Chuan Ma
* [QUICR](https://github.com/moq-wg/wg-materials/blob/main/interim-23-01/quicr-moq-interim.pdf), Suhas Nandakumar

**12:20 -  1:40  (Approximate) Lunch, not provided**

[MeetEcho Session -- Day 1 Afternoon](https://meetings.conf.meetecho.com/interim/?short=9f2f22d9-18f0-454f-b22f-e9f8b5a5020e)

 **1:40 -  2:00  [Requirements Draft](https://github.com/fiestajetsam/draft-gruessing-moq-requirements), Spencer and James**
 * [Open Issues](https://github.com/fiestajetsam/draft-gruessing-moq-requirements/issues)

**2:00 - 4:45: Base Protocol**

* 2:00 -  3:00  [Warp Draft](https://kixelated.github.io/warp-draft/draft-lcurley-warp.html) [Presentation](https://docs.google.com/presentation/d/1z4_uK4Tibe3QfqtNLR4EoyJlzBrQevCBaB3j5z83pLc/edit?usp=sharing) and Open Discussion, Luke Curley, Victor Vasiliev
* 3:00 -  3:20  (Approximate) Break
* 3:20 -  4:45  Issues list discussion, including open PRs
 
*Please file issues in the WARP repo and tag them per Ted's email*

**4:45 -  5:00**

Chair wrap-up and agenda adjustments for Day 2

-- Room closes at 5:00pm --


## Wednesday, February 1:

[Zoom Link](https://fb.zoom.us/j/94595516261)

Passcode: 553992

[MeetEcho Session -- Day 2 Morning](https://meetings.conf.meetecho.com/interim/?short=1db9c18d-bdb5-4c0c-83f6-f14ad9e45f74)

[Notes -- Day 2](https://notes.ietf.org/notes-ietf-interim-2023-moq-05-moq)

 **9:00 -  9:30: Room and Check-in open**

**9:30 - 11:00: Agenda Bash and Object model:**

Among the open questions:
* Do we need to have a protocol-level model for the composition of emissions that is consumed by an application.  (e.g. a videoconference with multiple publishers or a composed application of source + translation overlay)
* How long-lived or unique do identifiers need to be for a composition of emissions (e.g. Broadcast with both live commentary and closed captions or a Zoom meeting with multiple participants)?   How about for a single resource within the composition (the closed captions, or the resources sent by a single member of a video conference)?
*	How do you re-establish a session?
* Where does media format negotiation occur and when in the protocol flow?
*	How does priority get signaled to end consumers?  To intermediate network elements?

**11:00 - 11:15: (Approximate) Break**

**11:15 - 12:30:  Relays, Caches, and other middleboxes: Who needs to know what when?**

Among the open questions:
* Are they different behaviors for these that require different protocol behaviors? (e.g. a B2B UA might be a client and server from the point of view of the protocol, with an independently addressable set of resources).
* Are there ingest middleboxes as well as fan-out relays?  Are there some boxes that do both?  Do these need to be addressable by other protocol participants in different ways?

**12:30 - 1:45 (Approximate) Lunch, not provided**

[MeetEcho Session -- Day 2 Afternoon](https://meetings.conf.meetecho.com/interim/?short=120cc293-8cf9-4d01-95bd-a53e860f90ee)

**1:45 - 1:55 Agenda Bash and Scribe Selection**

**1:55 - 2:05: Discussion of call for adoption for requirements draft**

**2:05 - 3:00: Discussion of Warp architectural issues**

**3:00 - 3:15: (Approximate) Break**

**3:15 - 4:15: Discussion of Warp architectural issues...continued**

**4:15 - 4:45: Interim assigments**

**4:45 - 5:00: Wrap Up**

-- Room closes at 5:00pm --

As Time Permits

[MoQ Relay Network Handling](https://www.ietf.org/archive/id/draft-defoy-moq-relay-network-handling-01.html), Xavier De Foy
