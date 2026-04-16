# Emergency Procedures

In emergency communications, **discipline saves lives**. The difference between chaotic and coordinated radio communications in a disaster situation can be decisive for the timely response of rescue services.

This page covers the fundamental principles, standard message formats, and rules of conduct on an EmComm net.

---

## Golden Rules of EmComm Communication

### 1. Listening is primary

Before you transmit anything — listen. Find out:
- Is the frequency already in use?
- Is there a Net Control Station (NCS)?
- What type of traffic is there — routine, urgent, priority?

Rule: **90% of the time you listen, 10% you transmit.**

### 2. Short, clear, no jargon

EmComm communication is not a nuanced conversation — it is the transmission of information under stress. Use:
- **Standard phrases** (not improvisation)
- **Phonetic alphabet** for spelling critical data
- **Short sentences** — one message, one idea
- **Numbers spoken distinctly** — "one-zero-two" not "one hundred and two"

### 3. Write everything down

Every QSO in EmComm must be documented:
- UTC time
- Callsign of the sender
- Message content
- Action taken / forwarded to whom

A paper log is a backup when the laptop fails. Always have a notebook and pen.

### 4. Do not transmit without NCS permission

When a Net Control Station is operating, **all communication goes through the NCS**. Do not call other stations directly, do not relay messages without announcing, do not check into the net and immediately start transmitting.

!!! danger "Frequency stepping = chaos"
    Simultaneous transmission by multiple stations (carrier clash) results in an unintelligible signal and a lost message. In an EmComm situation that means lost information about casualties or locations. Maintain discipline.

---

## Message Priority

Messages are classified by urgency:

| Priority | Name | Description | Example |
|---|---|---|---|
| 🔴 1 | **DISTRESS / MAYDAY** | Immediate danger to life | "Mayday, mayday — vessel sinking, 12 persons on board" |
| 🟠 2 | **URGENCY / PAN-PAN** | Urgent situation, no immediate threat to life | "Pan-Pan — passenger with cardiac arrest, need ambulance at location X" |
| 🟡 3 | **SAFETY / SÉCURITÉ** | Warning of danger to others | "Sécurité — earthquake recorded, possible road damage on route Y" |
| 🟢 4 | **WELFARE** | Status information about casualties / injured | List of evacuees, infrastructure condition |
| ⚪ 5 | **ROUTINE** | Routine coordination and logistics | Frequency change, station status, relay request |

---

## Standard Message Formats

### MAYDAY call

Use exclusively for immediate danger to life:

```text
MAYDAY MAYDAY MAYDAY
This is [callsign]
Mayday — [description of situation in 1-2 sentences]
Our position is [coordinates or location description]
There are [number of persons] at this location
We require [food/water/medical aid/evacuation]
[callsign], over
```

### PAN-PAN call

For urgent situations without immediate threat to life:

```text
PAN-PAN PAN-PAN PAN-PAN
All stations, this is [callsign]
Pan-Pan — [description of situation]
Location: [description]
[Request for assistance]
[callsign], over
```

### IARU Standard EmComm Message

For structured transmission of information through the net (written — Winlink or relay):

```
1. PRECEDENCE: [Routine / Welfare / Priority / Emergency]
2. FROM: [callsign]
3. TO: [callsign or institution]
4. DATE/TIME (UTC): [DD/MMM/YYYY HH:MM]
5. RECEIVED VIA: [relay station callsigns]
6. MESSAGE:
   [Clear, brief message. One idea per sentence.
    Do not use abbreviations the recipient may not know.]
7. END OF MESSAGE
8. [sender's callsign]
```

!!! example "Example IARU EmComm message"
    ```
    1. PRECEDENCE: Priority
    2. FROM: 9A7YY
    3. TO: 9A1XX (NCS)
    4. DATE/TIME: 29/DEC/2024 14:35 UTC
    5. RECEIVED VIA: Direct
    6. MESSAGE:
       Reporting from location Petrinja, Moslavačka Street.
       Building at number 22 partially collapsed, I can see 3 survivors.
       Access difficult — street blocked by rubble.
       Coordinates: 45.4417 N, 16.2744 E.
       Heavy machinery required for access.
    7. END OF MESSAGE
    8. 9A7YY
    ```

---

## Phonetic Alphabet (ICAO/NATO)

In EmComm communication, every letter that could be misheard must be spelled using the phonetic alphabet:

| Letter | NATO | Letter | NATO |
|---|---|---|---|
| A | Alpha | N | November |
| B | Bravo | O | Oscar |
| C | Charlie | P | Papa |
| D | Delta | Q | Quebec |
| E | Echo | R | Romeo |
| F | Foxtrot | S | Sierra |
| G | Golf | T | Tango |
| H | Hotel | U | Uniform |
| I | India | V | Victor |
| J | Juliet | W | Whiskey |
| K | Kilo | X | X-ray |
| L | Lima | Y | Yankee |
| M | Mike | Z | Zulu |

Numbers are spoken clearly: **"niner"** for 9 (to avoid confusion with German "nein"), **"fife"** for 5 (clearly distinct from "fire").

---

## Special Rules on EmComm Frequencies

- **Never test your antenna** by transmitting on an EmComm frequency — it interferes with the net
- **Do not use** the frequency for routine contacts except when called by NCS
- **If you hear a MAYDAY** — stop transmitting, listen, and write down the information
- **Relay responsibility** — if you hear a distress call and NCS has not acknowledged it, it is your duty to act

!!! note "Legal aspect"
    Rendering assistance to persons in distress is a moral and in some jurisdictions a legal obligation for radio operators. Ignoring a MAYDAY you received without taking action is not acceptable.

---

## Training and Preparation

EmComm skills fade without regular practice. Recommended minimum:

- **Weekly**: Check in to the local EmComm net — just confirm your presence
- **Monthly**: Club EmComm exercise with message traffic
- **Annually**: Field Day (deploying a portable station without mains power)

---

## Related Topics

- [RMZO](rmzo.md) — Croatian EmComm organisation and frequencies
- [Winlink](winlink.md) — sending structured messages digitally
- [Portable Operations](../activities/portable.md) — portable station
