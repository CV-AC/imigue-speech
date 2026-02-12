# iMiGUE-speech: A Spontaneous Speech Dataset for Affective Analysis

This dataset is an extension of the iMiGUE dataset, providing a spontaneous affective corpus for the study of emotional and affective states. The new release focuses on speech and enriches the original dataset with a variety of metadata, including speech transcripts, speaker-role separation between interviewer and interviewee, and word-level forced alignments. The dataset contains the annotations described in the next section.

## Audio metadata/annotations for iMiGUE-Speech

| Type | Tool | Added metadata / output |
|---|---|---|
| Audio standardization | ffmpeg | Extracted audio; normalized format (1-channel PCM, fixed sampling rate). |
| Speaker diarization | `pyannote.audio` | Speaker-labeled time segments (e.g., `SPEAKER_00`). |
| Overlap detection | `pyannote.audio` | Intervals of simultaneous speakers. |
| VAD | `pyannote.audio` | Speech regions for removing silence/background noise. |
| Segment-level ASR | Whisper Large | English transcripts aligned to speech segments. |
| Segment-level TextGrid | Praat format | Unified tiers: diarization, overlap, VAD, transcripts. |
| Word-level alignment | MFA | Word boundaries from audio + Whisper transcripts. |
| Word-level TextGrid | MFA output | Separate tiered TextGrid with word and phone alignments. |
| Role identification | Heuristic | Longest cumulative speaking time mapped to athlete. |
| Speaker-specific clips | Custom | Disjoint athlete vs. journalist audio segment sets. |
| Segment indexing | Custom | Sequential IDs (e.g., `segment_001`). |

## Using the dataset and licensing
To access the dataset, please contact X to sign the license agreement. Once the agreement is signed, you will be granted access to the full dataset.

## Citing and repository information

This repository contains the data described in the paper:

Kakouros, S., Kang, F., & Chen, H. (2026). [iMiGUE-Speech: A Spontaneous Speech Dataset for Affective Analysis](https://arxiv.org/abs/2211.01756). *Accepted for presentation in Speech Prosody 2026*.

**Abstract:**  *This work presents an extension of the iMiGUE dataset, providing a spontaneous affective corpus for the study of emotional and affective states. The new release focuses on speech and enriches the original dataset with a variety of metadata, including speech transcripts, speaker-role separation between interviewer and interviewee, and word-level forced alignments. To demonstrate the utility of the dataset and establish initial performance benchmarks for the iMiGUE-Speech extensions, we introduce two affective state evaluation tasks to facilitate comparative evaluation: Speech Emotion Recognition (SER) and transcript-based sentiment analysis. These tasks leverage state-of-the-art pre-trained representations to assess the dataset’s capacity to capture spontaneous affective states from both acoustic and linguistic modalities. The extended dataset will be made publicly available to support future research in the study of affect and related fields.*

If you find the method useful, please cite:

```
@article{kakouros2026speech,
  title={iMiGUE-Speech: A Spontaneous Speech Dataset for Affective Analysis},
  author={Kakouros, Sofoklis and Kang, Fang and Chen, Haoyu},
  journal={arXiv to be added},
  year={2026}
}
```
