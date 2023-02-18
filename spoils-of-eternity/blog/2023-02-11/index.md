---
slug: February 2023
title: February 2023
# authors: [hoffchops]
tags: [update]
---

Getting back into it after taking some time off over the winter. Happy to come back to this with fresh eyes and a renewed perspective, and see how much was done before taking a break for the winter. 



## TODO For development purposes
1. Create a new `Equipment Item Interface` script to replace the existing. Merge functionality from the new `Item Slot Interface Controller` which was created for the new interface and layout and likely contains the appropriate shader logic for highlighting the selected slot. Otherwise, can leverage the existing functionality that was built for the equipment item slot. 
2. Will also probably want to rewrite the `Player Equipment Interface Controller`, but there's certainly some logic that I don't want to rewrite (calculating item stat deltas comes to mind).
3. Need to figure out what buttons will appear in the equipment interface. The wireframes have a button which would display other items of the selected slot, which hasnt been developed yet. 

## Questions/Decisions
1. 

## Bugs/Fixes
1. Omnisharp was throwing an error which I resolved by setting `"omnisharp.useGlobalMono"` in `settings.json` to `1.39.2`. It was previously set to `latest`. I did this because of the instructions at https://github.com/microsoft/vscode/issues/170031. I probably want this to eventually be set back to latest