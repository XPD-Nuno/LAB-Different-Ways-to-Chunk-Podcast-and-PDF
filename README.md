# Different Ways to Chunk Podcast and PDF

## About This Lab
This lab compares different chunking strategies for two sources:
- a PDF with structured policy content
- a podcast transcript with conversational content

The notebook explores fixed-size chunking, recursive chunking, and token-based chunking, then compares the results so you can see how each strategy behaves on different text types.

## Problem Being Solved
The goal is to find chunking strategies that preserve meaning and structure as well as possible.

- The PDF is dense and structured, so the chunking method should keep headings, numbered requirements, and related content together.
- The podcast is conversational, so the chunking method should preserve sentence flow and speaker-style progression instead of cutting the text arbitrarily.

The notebook measures chunk counts, chunk sizes, overlap cost, and boundary breaks to support a recommendation for each source.

## How To Run
1. Open `chunking_strategies.ipynb`.
2. Make sure the input files exist in `data/`:
   - `trustworthy_ai.pdf`
   - `trustworthy_ai_podcast.m4a`
3. Make sure your `.env` file contains the OpenAI API key if you want the notebook to regenerate the transcript.
4. Run the notebook cells from top to bottom.
5. The podcast transcript and split transcript parts will be written to `outputs/`.

## Key Files
- `chunking_strategies.ipynb`: main analysis notebook
- `outputs/podcast_transcript.txt`: combined transcript generated from the podcast parts
- `outputs/podcast_transcript_part_*.txt`: transcript files for each podcast chunk
- `outputs/podcast_parts/`: audio parts used to generate the transcript
