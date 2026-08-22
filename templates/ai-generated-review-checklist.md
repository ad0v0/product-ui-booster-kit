# AI-Generated Code Review Checklist

Quick-scan checklist for reviewing UI work produced by an AI coding assistant. Not a full manual review and targets failure modes specific to AI-generated output.

## Before you start

- [ ] **New feature or change to existing one?** — if it's a fix/change, every
      check below applies not only to the new piece, but to the surrounding existing
      functionality: confirm nothing that worked before is now broken.

## In the code

- [ ] **States beyond happy path** — loading, error, empty, and permission-limited
      states are explicitly present.

- [ ] **Result matches your actual intent, not just your literal prompt** —
      wherever your request left something unspecified, the AI still had to pick
      _something_ concrete to fill that gap on its own. Check whether that specific
      choice is what you meant — don't assume it's fine just because the code runs.

- [ ] **Consistency with existing patterns** — does this behave like the
      equivalent component/interaction elsewhere in the codebase, or did the AI
      invent its own approach?

- [ ] **Multi-step / async edge cases** — does the UI prevent a duplicate
      submission if the user clicks twice? What happens if multiple requests
      overlap (race conditions)? What happens if the user leaves or reloads
      mid-flow?

- [ ] **Human-readability of the code itself** — could someone else understand
      this in six months, or is it technically correct but "overexplainedly" written?

## In the browser

- [ ] **Cross-browser check** — AI defaults to whatever it "knows" works, which
      can include newer CSS/JS features supported only in Chrome. Verify the result
      actually renders/behaves the same in the browsers you support, not just the
      one you tested in.

- [ ] **Responsive across real viewports** — not just resize, but genuinely
      different widths.

- [ ] **Content overflow under varying content volume** — test with content
      amounts the layout wasn't designed around (e.g. a grid built for 4 items
      gets 5; a label gets a much longer string than the example used).

- [ ] **Real vs. superficial accessibility** — attributes present, but is
      keyboard navigation and focus actually verified in-browser, not just visible
      in markup?
