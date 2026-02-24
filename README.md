# name
podcast-to-ebook 

# description
Convert an English podcast transcript into a Chinese business biography eBook.  Designed for English podcast manuscripts exceeding 20,000 words，the process automatically completes three stages: translation and structuring, biography writing, and cover design. Each stage produces a file and proceeds only after manual confirmation before moving on to the next step.

# File Structure Reference
podcast-to-ebook/
├── .claude/
│   └── skills/
│       └── SKILL.md                  ← This file
├── assets/                          
│   ├── cover_reference*              ← Reference cover images (optional)
│   └── cover_[name].png              ← Store cover image here (manually saved by user)
├── output/                           ← Output files for each stage
│   ├── 01_translation_[name].md
│   └── 02_biography_[name].md
├── references/                       ← Reference materials
│   ├── translation_guide.md          ← Translation guidelines (used in Stage 1)
│   ├── biography_writing_style.md    ← Biography writing style guide (used in Stage 2)
│   └── style_examples.md             ← Walter Isaacson style reference excerpts (used in Stage 2)
├── scripts/                          ← Automation scripts (for future expansion)
└── src/                              ← Source materials
    └── [podcast_name]_transcript.txt
