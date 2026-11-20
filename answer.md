# Answer: Leveraging AI to Improve Efficiency and Quality

**Question:** Please share a recent example of how you leveraged AI to improve efficiency or quality in your work. What problem were you solving, how did you use the tool, and what aspects still required your direct input or judgment?

**Sources used:** [christinenoh.com](https://christinenoh.com) — home (Lab / Musear), Creator Studio case study + “How I work with AI,” Email A/B and Comment to DM reflections, resume, colophon, `llms.txt`, and Creator Studio presentation decks.

---

## Problem

I’m a Senior Product Designer for Gen AI and 0→1. At Kajabi I led **Creator Studio** — the company’s first paid AI product — from concept through GA. That work taught me that AI is only useful when people stay in control: assistive, not autonomous; editable outputs; clear progress, error, and retry for long-running jobs.

Since September 2026 I’ve been designing and building independently with Figma, Claude, Xcode, and Cursor. The recent problem I was solving: **validate a voice-AI idea fast enough that I don’t over-invest in polish before the core loop works.**

That idea is **Musear** — an iPhone proof of concept that gives Muse, an AI assistant, an ear and a voice, with no extra hardware. Say “Hey Muse,” speak, and hear Muse answer back. The risk wasn’t the brand or the Figma screens. It was feasibility: call → speak → hear back. If that failed, I needed to fail fast and move on.

A parallel problem was rebuilding my own portfolio site without templates or page builders — every interaction intentional — while still moving quickly.

## How I used the tool

I used AI the same way I design AI products: **AI drafts, humans own it.**

### Musear (Claude + Xcode)

1. **Feasibility first.** I coded and tested the core loop in Xcode with Claude before investing in full UX in Figma. Once the proof of concept works, I’ll connect Claude to Figma through MCP to design properly. If it doesn’t, I kill the idea.
2. **Design while building.** Prototyping in code with Claude let me feel the product before the debate got long. In the first build, I couldn’t tell if Musear was actually listening. Designing and coding at the same time caught a missing “listening” indicator — a gap I’d normally only find after real users tried it.
3. **Raise the starting line.** Claude handled first-pass Swift and wiring so I spent my time on voice UX, trust, and whether the experience felt human.

### Portfolio (Cursor + Claude)

I design every screen and make every call. AI pair programmers help me build: **Cursor** for the first version of [christinenoh.com](https://christinenoh.com), **Claude** for the 2026 refresh (Shipped/Lab layout, copy edits, video optimization), plus an in-progress gesture mode that runs hand tracking entirely on-device.

### Continuity with Creator Studio

This isn’t a side hobby disconnected from shipped work. On Creator Studio I drove the principle that creators must edit what AI creates — never the final author — and built Kajabi’s first AI design system patterns (AI intake without prompt-engineering, generation states, async toasts, editable outputs, media-type picker). Research showed creators preferred offerings built from **their existing content** over blank-page AI. Same rule I use myself: context beats prompting; taste picks what ships.

In my case-study reflections I wrote that if I built Creator Studio or the Visual Editor today, I’d prototype the hard interaction in code with Claude in week one and put something real in front of creators and engineering earlier. Musear is me practicing that lesson.

## What still required my direct input and judgment

- **Ship or kill.** Whether Musear’s loop is worth building at all — and when to stop.
- **Product and interaction judgment.** What “listening” should feel like; when silence is confusing; what trust looks like in a voice UI.
- **Taste.** AI can produce a hundred options; knowing the audience and what “good” looks like is the differentiator. On Creator Studio that meant insisting on editable AI and pivoting from clip maker to full-funnel content (usage doubled after that pivot). On Musear and the portfolio, it means every screen and every call is mine.
- **Strategy and honesty.** Co-writing strategy and pricing, running creator sessions, and being clear about what outcomes we measured vs. what we didn’t claim — judgment AI can’t own.
- **Responsibility.** AI brings speed and range. I bring voice, judgment, and accountability for what ships.

## Outcome

Efficiency: I get to a testable loop in days instead of waiting for a perfect Figma file or a vendor decision.  
Quality: building with Claude surfaces UX gaps (like the listening state) earlier than a design-only path.  
Principle: the leverage isn’t “let AI do the work.” It’s raising the starting line so human judgment goes where it matters — direction, taste, and ownership of what ships.
