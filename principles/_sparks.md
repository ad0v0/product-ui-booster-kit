# Sparks — raw candidates.

# Each one graduates into its own file once it survives the test:

# strip the context — does the claim still hold?

1. Trust is accumulated predictability — every interaction where the UI does what it earlier taught the user to expect adds to it; every time user questions UI it subtracts, regardless of whether the underlying result was technically correct.

2. Visual completion is not functional completion — UI can look finished (in accordance with every screen design) while missing the states that become visible only under real use: interaction, errors, partial data, permission limits, slow network, etc.

3. The happy path is for the demo, not for the product — real usage lives outside the happy path and is the real priority to address.

4. Consistency of behavior is a promise — once a user learns how something behaves, the interface implicitly promises it will keep behaving that way; breaking it means breaking the promise.

5. Feedback closes the loop — any action that was triggered by user without a visible confirmation or change reads as "it didn't work" regardless of whether it actually did.

6. Ambiguity is the interface's problem, not the user's — any point where a user has to guess or interpret is a failure of information design, not a lack of attentiveness.

7. State is a design object, not a side effect of code — how many states a screen has (loading, empty, partial, error, stale, permission-limited, success) should be an explicitly designed decision, not something inherited from whatever the backend happens to return.
