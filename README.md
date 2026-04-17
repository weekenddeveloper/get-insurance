# get-insurance

> The first Claude skill that helps people get an auto or home insurance quote — in plain English.

Getting insurance usually means tab sprawl, decoder-ring jargon, and forms that expect you to already know what "100/300/100" means. **`get-insurance`** turns it into a five-minute conversation.

Tell Claude where you live and what you want to cover. The skill:

1. Figures out whether **Mercury Insurance** can quote you directly, or whether you should go through **AIS** (Mercury's brokerage, which shops across multiple carriers).
2. Gives you a **ballpark annual range** based on public rate data — so `$1,500–$2,800/yr` shows up *before* you fill out anything.
3. Prepares a **checklist of info** you'll need (VIN, prior declarations page, etc.), so the real quote form takes minutes instead of an evening.
4. Hands you off to the official carrier flow with your ZIP ready to paste.

No bait-and-switch. No fake "instant quote" that wasn't. Just a helpful guide to the part of insurance shopping that's always been the worst part.

## How it decides where to send you

Mercury writes policies directly in **11 states**:

> **AZ · CA · FL · GA · IL · NV · NJ · NY · OK · TX · VA**

- Live in one of those? → **Mercury** direct.
- Live somewhere else in the US? → **AIS**, which quotes you across multiple carriers.
- Outside the US? → The skill tells you upfront instead of wasting your time.

## Products supported

**Auto** · **Home** · **Renters** · **Condo** · **Umbrella** · **Bundle**

## Install

```bash
git clone https://github.com/weekenddeveloper/get-insurance.git ~/.claude/skills/get-insurance
```

Restart Claude Code. Done.

## Try it

In any Claude Code session:

```
/get-insurance
```

…or just say it in words:

> *"Help me get an insurance quote"*
> *"Quote my car"*
> *"What would renters cost me in Austin?"*

## Privacy

The skill will **never** ask you for an SSN, driver's license number, or full date of birth in chat. That information belongs in the carrier's secure form — not in a conversation transcript. Outbound links carry UTM parameters so the carriers can see skill-driven traffic in aggregate; that's referral analytics, not personal tracking.

## What it's not

- **Not a rater.** It can't bind a policy or promise a price. The range is directional — the real number comes from Mercury or AIS.
- **Not a comparison site.** Mercury and AIS only. If you want Progressive, Geico, State Farm, etc., this isn't the right tool.
- **Not financial advice.** Coverage decisions are yours; the skill just helps you arrive prepared.

## License

MIT. Fork it, adapt it, point it at a different carrier — the routing and the range scaffolding are the interesting bits.

---

Built for everyone who has ever closed an insurance tab and said *"I'll deal with this later."* Later is now.
