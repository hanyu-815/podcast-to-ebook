# name
podcast-to-ebook 

# description
Convert an English podcast transcript into a Chinese business biography eBook.  Designed for English podcast manuscripts exceeding 20,000 words，the process automatically completes three stages: translation and structuring, biography writing, and cover design. Each stage produces a file and proceeds only after manual confirmation before moving on to the next step.

# File Structure Reference
podcast-to-ebook/
├── .claude/
│   └── skills/
│       └── SKILL.md                 # Core instructions & AI persona
├── assets/                          # Visual media assets
│   ├── cover_reference* # Reference images for cover design
│   └── cover_[name].png             # Manually saved final cover image
├── output/                          # Processed output files
│   ├── 01_translation_[name].md     # Stage 1: Translated transcript
│   └── 02_biography_[name].md       # Stage 2: Final biography draft
├── references/                      # Knowledge base & guidelines
│   ├── translation_guide.md         # Formatting & translation rules
│   ├── biography_writing_style.md   # Biography writing instructions
│   └── style_examples.md            # Walter Isaacson style excerpts
├── scripts/                         # Automation & utility scripts
└── src/                             # Raw source materials
    └── [podcast_name]_transcript.txt # Original podcast transcript

