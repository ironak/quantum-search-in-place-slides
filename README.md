Slides for "Quantum Search with In-Place Queries", published and presented at TQC 2025 in Bangalore. If this code helps you make your own presentations, please send me an email to let me know! Tell all your friends about manim so more research talks incorporate clear visuals.

# Quickstart
If you don't have uv, install it (https://docs.astral.sh/uv/#installation). After cloning this repo, run the following commands from a terminal in the repo directory:
```
uv venv
source .venv/bin/activate
uv pip install jupyter
uv pip install manim
uv pip install -U "manim-slides[pyside6-full]"
```
You might need to install cmake, pkg-config, and cairo using your favorite package manager before installing manim.

To run my scripts, you'll need to edit ```.venv/lib/python3.13/site-packages/manim/utils/color/manim_colors.py``` to add the colors IN_PLACE and XOR. Add them before _all_manim_colors is defined.
```
#ronakr colors
XOR = ManimColor("#56B4E9")
IN_PLACE = ManimColor("#E69F00")
```

# Exporting

For compiling to pptx:
```
manim-slides convert TitleSlide Complexity QueryComplexity QueryModels KeyQuestion Comparisons LeadingCand FuncErasIntro Plan GroverSection StepThruGroverBar GroverBreakdown AlgSection ShiftDemo OurAlg OurBars LBSection FuncErasToXOR OurLB ApplyingAlg FutureWork ThankYou /mnt/c/Users/irona/Downloads/tqc-presentation-V3-qh-2.pptx
```

RPE version:
```
manim-slides convert TitleSlide Complexity QueryComplexity QueryModels KeyQuestion Comparisons TruckBoat Plan GroverSection StepThruGroverBar GroverBreakdown AlgSection ShiftDemo OurAlg OurBars LBSection FuncErasToXOR OurLB ApplyingAlg FutureWork ThankYou /mnt/c/Users/irona/Downloads/rpe-1.pptx
```

For compiling to html:
```
manim-slides convert TitleSlide Complexity QueryComplexity QueryModels KeyQuestion Comparisons LeadingCand FuncErasIntro Plan GroverSection StepThruGroverBar GroverBreakdown AlgSection ShiftDemo OurAlg OurBars LBSection FuncErasToXOR OurLB ApplyingAlg FutureWork ThankYou ~/public_html/InPlaceSearch.html --offline
```

Visa version:
```
manim-slides convert TitleSlide Complexity QueryComplexity QueryModels KeyQuestion Comparisons TruckBoat GroverSection QuantumPrimer StepThruGroverBar GroverBreakdown AlgSection ShiftDemo OurAlg OurBars FutureWork ThankYou /mnt/c/Users/irona/Downloads/visa-in-place.pptx
```