# Contribution 1: UI: add a svg icon for the crash cymbal

**Contribution Number:** 1  
**Student:** Jean Joiles  
**Issue:** https://github.com/Babali42/DrumBeatRepo/issues/511  
**Status:** Phase III Complete

---

## Why I Chose This Issue

I chose issue #511, "UI: add a svg icon for the crash cymbal," because it stood out to me the most out of the available issues. I love music, so I thought working on a music-related project would be both interesting and enjoyable. The issue focuses on adding a missing crash cymbal icon to the Rock Variation Pattern, even though the MIDI note for it is already set up.

I also chose this issue because it seems like a good opportunity to build on my frontend skills while learning how to work with an existing codebase. Since it is labeled as a "good first issue" and has a clear goal, I felt like it would be a good starting point for my first open-source contribution. Through this issue, I hope to become more comfortable navigating someone else's code, working with SVG assets, and understanding how UI changes are made within a larger project.
---
## Understanding the Issue

### Problem Description

Issue #511 focuses on the missing SVG icon for the crash cymbal in the Rock Variation Pattern. The crash cymbal is already included as a MIDI note, but it does not have the appropriate image displayed in the user interface. This makes the crash cymbal look incomplete compared to the other instruments in the pattern.

### Expected Behavior

The crash cymbal should have its own SVG icon displayed in the Rock Variation Pattern, similar to the other drum instruments.

### Current Behavior

The crash cymbal is included in the pattern, but the corresponding crash cymbal SVG image is missing from the interface.

### Affected Components

The issue affects the frontend of the DrumBeatRepo application, specifically the assets and UI components responsible for displaying instrument images in the drum patterns.
---
## Reproduction Process

### Environment Setup

In class, we worked through the DrumBeatRepo project using VS Code and the `cymbal-image` branch. The project uses a Scala engine and an Angular frontend. According to the project's README, the Scala engine is built using `sbt fastLinkJS`, and the Angular frontend is started using `npm run start`. I also cloned the repository locally in VS Code so I could review the project files and the branch.

### Steps to Reproduce

1. Clone and open the DrumBeatRepo project in VS Code.
2. Navigate to the `engine` directory.
3. Run `sbt fastLinkJS` to build the Scala engine.
4. Navigate to the `frontend` directory.
5. Run `npm run start` to start the Angular application.
6. Open the application at `http://localhost:4200`.
7. Navigate to the Rock Variation Pattern.
8. Locate the crash cymbal in the pattern.
9. Compare the crash cymbal with the other drum instruments that already have SVG icons.
10. Observe that the crash cymbal is included in the pattern but is missing its corresponding SVG icon.

**Expected Result:** The crash cymbal should display its own SVG icon like the other drum instruments.

**Actual Result:** The crash cymbal is present in the pattern, but its SVG icon is missing from the user interface.

### Reproduction Evidence

- **Commit showing reproduction/Branch Link:** https://github.com/shanker-codepath/DrumBeatRepo/tree/cymbal-image
- **Screenshots/logs:** The issue and solution were worked through during the in-class walkthrough.
- **My findings:** From working through the issue in class, I found that the crash cymbal was already included as a MIDI note, but it was missing the SVG icon needed for it to display like the other instruments. Looking at how the other instrument icons were set up helped show how the crash cymbal icon could be added while keeping the same structure already used in the project.

---

## Solution Approach

### Analysis

After reviewing the issue and going through it in class, I found that the main problem was not with the crash cymbal being included in the pattern. The crash cymbal was already configured as a MIDI note. What was missing was the SVG image for it in the frontend. Since the other instruments already had their own icons, they provided a good example of how the crash cymbal could be added.

### Proposed Solution

The solution would be to add the crash cymbal SVG image to the frontend and connect it to the crash cymbal using the same approach that is already used for the other instrument icons. Following the existing structure would keep the change consistent with the rest of the project.

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** The crash cymbal is already represented as a MIDI note in the Rock Variation Pattern, but it is missing its corresponding SVG image in the user interface.

**Match:** I would look at how the existing drum instruments and their SVG images are set up in the frontend and use those as a reference for adding the crash cymbal.

**Plan:**
1. Find where the existing drum SVG images are stored in the frontend.
2. Review how the existing SVG images are connected to their corresponding instruments.
3. Add the crash cymbal SVG image to the appropriate location.
4. Connect the crash cymbal to the new SVG using the same structure as the other instruments.
5. Run the application and return to the Rock Variation Pattern.
6. Verify that the crash cymbal icon appears correctly.
7. Make sure the other instrument icons still display correctly.
8. Run the appropriate frontend tests to make sure the change does not cause any other issues.

**Implement:** Implementation will be completed in Phase III.

**Review:** I would review the changes to make sure they follow the existing structure of the DrumBeatRepo project and are consistent with the way the other instrument SVG images are handled.

**Evaluate:** I would run the application and verify that the crash cymbal SVG appears correctly in the Rock Variation Pattern. I would also make sure the other instrument icons continue to display correctly and run the appropriate frontend tests to check that nothing else was affected.

---
---

## Testing Strategy

### Unit Tests

- [x] Test case 1: Verify that the crash cymbal MIDI value maps to `assets/images/drums/crash.svg`.
- [x] Test case 2: Verify that the crash cymbal uses the new crash image instead of the default image.
- [x] Test case 3: Verify that the existing drum image mappings remain in place.

### Integration Tests

- [x] Verify that the crash cymbal image follows the same frontend image structure used by the other drum instruments.
- [x] Verify that the new crash cymbal SVG assets are correctly connected to the drum image pipe.

### Manual Testing

During the in-class walkthrough, the implementation was reviewed to confirm that the crash cymbal was mapped to the new crash image and that the light and dark SVG assets were added to the frontend.

---

## Implementation Notes

### Week [X] Progress

During class, we completed the implementation for Issue #511. The crash cymbal was already represented by MIDI values in the application, so the implementation focused on connecting those values to the correct image. The drum image pipe was updated to map the crash cymbal values to the new crash image. Light and dark versions of the crash cymbal SVG were also added to the frontend assets, and the existing unit test was updated to expect the crash cymbal image instead of the default image.

The main challenge was understanding how the existing drum images were connected to their MIDI values. Reviewing the existing mappings and tests helped show how the crash cymbal could be added while following the structure already used by the project.

### Week [Y] Progress

The completed changes were reviewed to confirm that the crash cymbal implementation followed the existing frontend structure and that the necessary image assets, mappings, and test updates were included.

### Code Changes

**Files modified:**
- `frontend/src/app/ui/pipes/drum-image.pipe.ts`
- `frontend/src/app/ui/pipes/drum-image.pipe.spec.ts`
- `frontend/src/assets/images/drums/crash-dark.svg`
- `frontend/src/assets/images/drums/crash-light.svg`

**Key commits:**  
https://github.com/shanker-codepath/DrumBeatRepo/commit/b59aaf31b18ac289dae77653635de0e3b691eaa1

**Approach decisions:** The implementation followed the existing structure used for the other drum instrument images so that the crash cymbal would be handled consistently with the rest of the frontend.

---
Pull Request
PR Link: [GitHub PR URL when submitted]
PR Description: [Draft or final PR description - much of the content above can be adapted]
Maintainer Feedback:
[Date]: [Summary of feedback received]
[Date]: [How you addressed it]
Status: [Awaiting review / Iterating / Approved / Merged]
---
Learnings & Reflections
Technical Skills Gained
[What you learned technically]
Challenges Overcome
[What was hard and how you solved it]
What I'd Do Differently Next Time
[Reflection on your process]
---
Resources Used
[Link to helpful documentation]
[Tutorial or Stack Overflow post that helped]
[GitHub issues or discussions that helped]
