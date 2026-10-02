# SoundCLIP project page update — 2026-10-01

Updated locally in `C:\Users\abc\projects\SoundCLIP-page` on the new branch `update-2026-10`. Nothing was pushed. The public site remains unchanged until the reviewer publishes this branch after Ali's review.

Session ID: `01a0fa0c-8128-76b1-8526-dfb35e8508fa` (`CODEX_SESSION_ID` / `CODEX_THREAD_ID`).

Base: `main` at `cb188db218f348a8debbe0c8814402ea6f1516c3`. Commit message: `Align with the current paper version (October 2026)`. No AI co-author trailers.

## Source and scope

The authority is the frozen ICASSP submission in `G:\My Drive\Godfile\CVs\publication_data\papers\icassp2027_soundclip_llava_token_substitution`: `main.tex`, its included sections and figure captions/tables, `main.pdf`, `figures/`, `NUMBER_LEDGER_2026-09-12.md`, and the author list in `SUBMISSION_FORM_2026-09-14.md`. The page uses the PDF/main.tex abstract, not the shorter portal abstract. The local paper source was read without modification.

The existing serif typography, colors, navigation, section/card layout, video examples, and encoder-button interaction are retained. The existing page sections remain, with a method section added for the submission figures. README top-level sections remain. No framework, dependency, or external script was added.

## Title, authors, venue, abstract, and links

| Item | Old | New |
| --- | --- | --- |
| Page heading | Can Sound Replace Vision in LLaVA With Token Substitution? | PROJECTED AUDIO TOKENS GAIN RETRIEVAL AND LOSE GROUNDED GENERATION IN MULTIMODAL LLMS |
| Browser title / README title | SoundCLIP: Can Sound Replace Vision in LLaVA With Token Substitution? | Same exact current paper title above; only the TeX forced line break becomes a space |
| Authors | Ali Vosoughi, Jing Bi, Pinxin Liu, Yunlong Tang, Chenliang Xu | Ali Vosoughi, Jing Bi, Pinxin Liu, Yolo Y. Tang, Chenliang Xu |
| Fourth-author website | `https://yunlong10.github.io/` | `https://yoloytang.me/` |
| Venue | No explicit venue line; paper/citation labels pointed to the earlier arXiv version | Preprint; submitted to ICASSP 2027 |
| Subtitle | A Systematic Investigation of Audio-Visual Alignment Trade-offs in Multimodal Systems | Replaced by the exact venue line |
| Abstract | Earlier two-paragraph superalignment/encoder-lineage narrative, quoted below | Current main.tex abstract verbatim after rendering TeX punctuation and normalizing whitespace; 1,694 characters |
| Primary paper links | `https://arxiv.org/abs/2506.10416` | `paper/main.pdf`, a byte-identical copy of the frozen submission |
| Earlier preprint | Presented as the current paper | Kept separately as “Earlier arXiv Version” / “Earlier Version” |
| Citation | Old title/author, article/arXiv metadata; HTML and README years differed | Matching `@unpublished{vosoughi2026soundclip}` entries, current title/authors, year 2026, exact venue note, current PDF URL |
| Footer | Institution, authors, resources | Adds [Ali Vosoughi’s Showcase](https://ali-vosoughi.github.io/) |

The dataset link remains `https://huggingface.co/datasets/ali-vosoughi/ave-2`. All current Ali author entries use **Ali Vosoughi**. Historical names are quoted in this report only to document the author correction.

## Removed or corrected claims in index.html

The quotations below come from the cloned `main` files. Each scientific or resource claim removed or corrected is recorded here, including repeated claims in different sections.

### Earlier abstract

> What happens when we push audio-visual alignment to its absolute limits? To systematically investigate this question, we needed datasets with granular alignment quality annotations, but existing datasets treat alignment as binary, either synchronized or not. To address this limitation, we developed a comprehensive dataset featuring detailed alignment scores that reveal the hidden spectrum of audio-visual perceptual correspondence. Using these precise scores, we create "superaligned" representations by training exclusively on the most perfectly matched audio-visual pairs, then conduct our systematic investigation into how this extreme alignment transforms perceptual model behavior across retrieval and generation tasks.

Replaced the entire opening paragraph with the submission abstract. The current paper presents a controlled frozen-model comparison; it does not claim exhaustive alignment limits, binary-only prior datasets, a new dataset contribution, or exclusive training on “superaligned” pairs.

> Our findings reveal that the initial architectural type of the encoder determines how it responds to the alignment process. Image-centric encoders demonstrate exceptional performance in cross-modal retrieval, but this intensive alignment causes compression of unique linguistic information and reduces the quality of their text description generation. In contrast, text-centric encoders maintain better balance between the two objectives, revealing a fundamental trade-off where excessive alignment with the visual manifold leads to improved retrieval capabilities, but simultaneously reduces the richness of acoustic and linguistic information necessary for quality text description generation.

Replaced the entire findings paragraph with the submission abstract. Removed causal information-compression and encoder-lineage claims. The current evidence reports retrieval and grounding contrasts with lower-bound/scorer caveats and no causal mechanism.

### Dataset and usage

> We introduce AudioVisual Event Evaluation (AVE-2), a dataset of 570,138 three-second audiovisual clips with fine-grained alignment annotations. Unlike existing datasets that treat alignment as binary, AVE-2 provides detailed alignment scores across five dimensions, enabling systematic investigation of audio-visual correspondence quality.

Corrected the name to Audio-Visual Event 2 and described the corrected local rebuild of 570,138 three-second AudioSet segments. Removed the new-dataset framing and alignment-quality/dimensionality claims. The current paper uses active-source fields for source recall and does not treat machine-generated alignment scores as ground truth.

> AVE-2 is now available on HuggingFace! Get started with our comprehensive dataset in just a few lines of code:

Removed the availability announcement and promotional wording; the dataset documentation and loading example remain.

> Load the dataset metadata and explore 570K samples with alignment scores instantly.

Replaced rounded 570K and instant-loading language with exact ledger-backed counts and neutral metadata instructions.

> Download chunked video files (237GB total) for complete audio-visual analysis.

Removed the unsupported 237GB size and complete-analysis claim; directs readers to the dataset’s media documentation.

> Filter by quality scores, explore alignment dimensions, and build your models.

Replaced quality-score filtering with inspection of visible and invisible active-source fields.

The old statistic labels “570K” / “Audio-Visual Clips”, “5” / “Alignment Dimensions”, “3” / “Seconds per Clip”, and “7” / “Demo Examples” were replaced with the ledger-backed segment, evaluation, generation, and geometry counts. Three-second segment duration remains in the prose. Demo ordinals and media identifiers remain identifiers rather than research measurements.

The old usage snippets also contained these unsupported or unnecessary display claims:

> # Load dataset with metadata (instant)

Removed the loading-speed promise.

> print(f"Temporal Alignment: {sample['temporal_alignment_score']}/10")

Removed the unledgered alignment-score scale and sample-score display.

> # Now includes video paths!

Removed the claim that loading metadata automatically reconstructs media paths.

> # Quality-aware filtering

Removed the filtering example with >= 8 thresholds for temporal alignment, spatial coherence, and physical causality; these are not current evaluation ground truth.

> GitHub Repository with Examples

Renamed to GitHub Repository without an unsupported resource-content promise.

The obsolete media reconstruction/install/verification snippets were simplified to the existing `load_dataset("ali-vosoughi/ave-2")` example and documentation links. No replacement storage size or quality threshold was invented.

### Key findings

> Our systematic investigation reveals a fundamental trade-off where excessive alignment with the visual manifold leads to improved retrieval capabilities, but simultaneously reduces the richness of acoustic and linguistic information necessary for quality text description generation.

Replaced the universal causal trade-off with the measured retrieval/grounding contrast within the tested configurations and explicitly named frozen LLaVA-1.6-Mistral-7B.

> Image-centric encoders (ImageBind, AudioCLIP, Wav2CLIP) demonstrate exceptional performance in cross-modal retrieval due to their inherent design for visual alignment, but this intensive alignment causes compression of unique linguistic information and reduces text generation quality. Text-centric encoders (CLAP, Whisper) maintain stronger linguistic authenticity and achieve better balance between retrieval and generation objectives.

Removed inherent-design, linguistic-compression, authenticity, and encoder-family superiority claims. The replacement reports ledger-backed R@1, B1, B2, and B3 for each encoder.

> The initial architectural type of the encoder determines how it responds to the alignment process. Encoders pre-trained with text supervision maintain stronger generative capabilities than those focused primarily on audiovisual alignment, highlighting the value of language exposure for generation tasks.

Removed the architectural-determinism and language-supervision advantage claims. The replacement describes paired geometry associations, explicitly without a causal mechanism.

> We establish a clear Pareto frontier for cross-modal learning, providing guidelines for choosing between retrieval accuracy and generative richness based on application needs. This challenges the assumption that stronger cross-modal alignment necessarily benefits all multimodal tasks.

Removed the Pareto-frontier assertion and broad theoretical challenge. The replacement states the evaluated scope, audio-aware-reference result, and backbone-stability qualification.

The headings “Performance Trade-offs”, “Architectural Insights”, and “Pareto Frontier Discovery” were replaced with “Retrieval and Grounded Generation”, “Representation Geometry”, and “Scope and Backbone Stability”.

> All code, data, and pre-trained models are made available to facilitate reproducibility and future research in audio-visual alignment.

Removed the blanket code/data/model availability claim. The section now links the current paper, earlier arXiv version, repository, and dataset documentation.

### Backbone correction

Neither cloned page file explicitly said “LLaVA-1.5”; therefore no nonexistent old sentence is attributed to the page. The old README said “Replace CLIP's [CLS] token with audio tokens in LLaVA”, and the main paper buttons opened the superseded version. The page, abstract, method, results, README, and primary PDF links now identify the actual frozen **LLaVA-1.6-Mistral-7B** probe. This also prevents the older linked paper’s backbone wording from being presented as the current method.

### Archived demonstrations

> Explore how different audio encoders (Raw vs Projected) generate different captions for the same audiovisual content. Click on any encoder mode button to see the generated caption.

The examples remain interactive but are explicitly labeled archived illustrations from the earlier page, not results from the current evaluation pool. Descriptions and source annotations are labeled earlier/generated; encoder label “WHISPERCLIP” becomes “WHISPER”.

> Mistral's analysis of sound sources in the audiovisual scene:

Changed in every example to “Earlier machine-generated source annotations:” to avoid assigning current validation or backbone provenance to these archived annotations.

Removed all unledgered alignment score badges and bars. Exact old values, in the displayed order Temporal / Spatial / Contextual / Causality / Visibility:

| Example / media ID | Old quoted badge | Old component values |
| --- | --- | --- |
| 1: Video ID: rvbmYs4Kl3Y (Segment 01) | “Alignment Score: 47.0/50” | “10/10”, “10/10”, “10/10”, “9/10”, “8/10” |
| 2: Video ID: IwqD859w2_E (Segment 02) | “Alignment Score: 44.0/50” | “9/10”, “10/10”, “8/10”, “9/10”, “8/10” |
| 3: Video ID: DDer7K8WG4I (Segment 02) | “Alignment Score: 46.0/50” | “10/10”, “10/10”, “9/10”, “9/10”, “8/10” |
| 4: Video ID: UorSpZVnX_M (Segment 02) | “Alignment Score: 46.0/50” | “9/10”, “10/10”, “10/10”, “9/10”, “8/10” |
| 5: Video ID: EQHrQIaQNv8 (Segment 03) | “Alignment Score: 45.0/50” | “10/10”, “10/10”, “8/10”, “9/10”, “8/10” |
| 6: Video ID: GJhYkfI7jpU (Segment 03) | “Alignment Score: 42.0/50” | “8/10”, “10/10”, “7/10”, “9/10”, “8/10” |
| 7: Video ID: AVL7Kbpw13U (Segment 01) | “Alignment Score: 42.0/50” | “8/10”, “10/10”, “7/10”, “9/10”, “8/10” |

These values were removed rather than substituted with aggregate experiment results. The old score-bar animation was removed with its unused display. Original videos and images remain unchanged.

The following archived description/caption passages were omitted with visible `[…]` markers, preserving the remaining generated text rather than inventing new outputs. The omitted numerical hallucinations have no ledger basis; other omissions remove level wording as requested.

> The tower has three levels, each adorned with ornate details such as statues and intricate patterns. At the top level, there are two bells hanging from what appears to be a small balcony or ledge. Below this, on the second level, there is another set of bells, also hanging from a similar structure.

> The clock hands are also moving, indicating the time as 11:10, which is a time when the clock's minute hand is on the number 11 and the hour hand is on the number 10.

> The main object in this image is a guitar, and it is sounding the note E4, which is also known as the musical note "E."

> The guitar is being played by a person whose hands are partially visible, suggesting that they are likely strumming or picking the strings to produce the E4 note.

> The clock's hands are black and are pointing to the 12 o'clock position, indicating the time as 12 o'clock.

> In general, the sound of a piano can be described as a rich, resonant, and dynamic musical instrument that can produce a wide range of volume levels and dynamic expression.

## Removed or corrected claims in README.md

> [Code is coming soon.. stay tuned]

Removed the future availability promise.

> This is the official project webpage for "Can Sound Replace Vision in LLaVA With Token Substitution?" featuring an interactive demonstration of our SoundCLIP framework and the fundamental trade-off between cross-modal retrieval and text generation.

Replaced with the exact current title and a scoped description of retrieval, grounded generation, and geometry in frozen LLaVA-1.6 with Mistral-7B, without a causal mechanism.

> **570,138 audio-visual clips** with revolutionary 5-dimensional alignment annotations

Replaced with the corrected local rebuild of 570,138 three-second AudioSet segments; removed hype and unledgered dimensionality.

> Now available on HuggingFace with comprehensive documentation and usage examples

Removed the availability claim; retained dataset links.

> Systematic scoring across: Temporal Alignment, Spatial Coherence, Contextual Relevance, Physical Causality, Sound Source Visibility

Replaced with active-source fields, evaluation/geometry use, and ledger-backed evaluation sizes.

> **Token substitution approach**: Replace CLIP's [CLS] token with audio tokens in LLaVA

Specified replacement of the visual class token with an audio token in frozen LLaVA-1.6-Mistral-7B, retaining selected visual patches.

> **Two alignment strategies**:

Renamed to “Two token constructions”.

> Projected: MLP projection to CLIP space (maximizes I(A;V), better retrieval)

Replaced with the three-layer MLP mapping to CLIP visual space. The current geometry evidence does not establish mutual-information maximization.

> Raw: Padded audio features (preserves H(A|V), better generation)

Replaced with padding/truncation to 1,024 dimensions without the learned visual mapping. Removed the conditional-entropy preservation claim.

> **Lightweight integration**: Only 1.9M parameters for projection layer

Removed the unverifiable parameter count and promotional qualifier. Replaced with five frozen encoders and the two verified token budgets.

> ### 3. Fundamental Trade-off Discovery

Renamed this contribution subsection “Retrieval and Grounded Generation”; all original top-level sections remain.

> **Retrieval vs Generation**: y = 0.163x + 11.867 relationship discovered

Removed the unverified regression law. Replaced with the ledger-backed retrieval and grounding changes.

> Each percentage-point gain in retrieval incurs ~0.163% loss in generation quality

Removed the unsupported fixed loss rate. Current results state relative B1/B3 reductions with scorer and backbone qualifications.

Old citation title, author name, arXiv journal metadata, and year were updated as recorded in the metadata table. Both current BibTeX blocks now match. “Live Demo” / “Interactive Demo” link labels in README became “Project Page”, reflecting that the interactive illustrations are archived.

## Figures and frozen PDF

The cloned page had **no displayed teaser or method image** to swap: its `images/` directory held seven demonstration JPGs, none referenced as a paper figure. The update adds the current paper’s teaser and method at the existing page width instead of falsely describing a replacement of nonexistent figure references.

| Role | Source in paper folder | New page asset | Treatment |
| --- | --- | --- | --- |
| Teaser | `figures/fig1_teaser_v2.png` | `images/fig1_teaser_v2.png` | Byte-for-byte copy; six labels positioned exactly as in `figures/fig1_teaser.tex`; current caption |
| Method | `figures/fig2_probe_v2.png` | `images/fig2_probe_v2.png` | Byte-for-byte copy; six labels positioned exactly as in `figures/fig2_probe.tex`; current caption |
| Current paper | `main.pdf` | `paper/main.pdf` | Byte-for-byte copy of the frozen submitted PDF; primary paper buttons link here |

The PNG artwork omits the labels added by LaTeX. Local HTML/CSS overlays preserve those labels without editing the image files. All seven original JPGs and seven original MP4s were retained byte-for-byte. No image or video was deleted.

The evidence figure was not added because it includes later quantities outside the September 12 ledger; the page instead reproduces the verified main result table. The full frozen paper remains the authority for its complete figures and tables.

PDF SHA256: `dd6a6168db5d61ab69eb0b259f3ed9680d7fa251330b00f7b723de65d9603ed6`. It also matches `submitted_20260914_paper5320/main.pdf` exactly. The frozen PDF and its historical bibliography were not edited.

## Number audit

Every displayed research quantity was checked against the ledger. Dates, citation keys, model/metric names, code syntax, CSS dimensions, demo ordinals, segment labels, and media IDs are identifiers or presentation data rather than new measured claims.

| Displayed quantity | Ledger rows |
| --- | --- |
| Five frozen audio encoders; five backbones; 7B–34B with stability qualification | A2, A10–A11, D22 |
| LLaVA-1.6 / Mistral-7B; three-layer MLP; 1,024 dimensions; 576 visual patches; k=15 and k=150 | B1–B2, B4–B6 |
| 570,138 three-second segments | F1 |
| 1,006 evaluation clips; 1,010 generation clip-segments; 3,568 disjoint geometry clips | A1, A7, C2–C3, C5 |
| Abstract ImageBind R@1: 0.10% → 15.7%; table: 0.10 → 15.71 | A3, C6; preserves the paper’s differing printed precisions |
| All main-table R@1, B1, B2, B3 entries | C6–C9 |
| B1 raw 0.113–0.132 → projected 0.062–0.088, relative decrease 23–53% | A4, C7, D2 |
| B3 raw 0.161–0.185 → projected 0.090–0.112, relative decrease 31–48% | A5, C9, D2 |
| B2 falls for four encoders; Wav2CLIP unchanged at printed precision | A6, C8 |
| Nine of ten audio-aware-reference cells | A9, D27; current paper explicitly identifies BLEU |

The current result table, each cell raw → projected:

| Encoder | R@1 (%) | B1 | B2 | B3 |
| --- | --- | --- | --- | --- |
| AudioCLIP | 0.00 → 1.19 | 0.125 → 0.088 | 0.219 → 0.204 | 0.161 → 0.111 |
| Wav2CLIP | 0.00 → 3.88 | 0.113 → 0.086 | 0.211 → 0.211 | 0.163 → 0.112 |
| ImageBind | 0.10 → 15.71 | 0.132 → 0.078 | 0.226 → 0.198 | 0.169 → 0.094 |
| CLAP | 0.10 → 1.99 | 0.129 → 0.071 | 0.225 → 0.199 | 0.185 → 0.107 |
| Whisper | 0.10 → 0.70 | 0.131 → 0.062 | 0.223 → 0.192 | 0.174 → 0.090 |

No former AudioCaps retrieval table, regression coefficient, parameter total, unledgered storage size, or demo alignment score is presented as a current result. The page retains CLAP/Whisper retrieval lower bounds, the CLAP scorer-family caveat, noncausal geometry wording, and raw-token generation stability.

## Validation

- Started `python -m http.server 8765 --bind 127.0.0.1` in the repository using a hidden process; fetched `/` and received HTTP **200**.
- Fetched every local asset path, including all retained original images/videos and the copied PDF: **17/17 HTTP 200** (nine images, seven videos, one PDF).
- Compared original image/video bytes against `main`: **14/14 unchanged**. Copied figures and PDF match their source bytes.
- Headless Edge/Playwright rendered the page at **1440×1000** and **390×844**; inspected desktop/mobile screenshots. No page-wide mobile overflow; the result table scrolls within its own container.
- Tested **70/70 encoder-mode buttons**; all display their corresponding archived caption and selected state. No browser JavaScript errors.
- Verified all internal fragment links resolve; both paper images load; no external scripts.
- Verified the exact title, ordered author list, venue, main.tex abstract, all twelve figure labels/positions, result table, dataset link, and footer showcase link.
- Checked HTML and README for prohibited venue/acceptance strings, Ali name variants, level wording, citation-count claims, and availability/job-search language: none remain. All Ali author entries use the requested printed name. PDF text was separately checked for the prohibited venue/acceptance strings and unexpected Ali-name variants.
- Independent paper/ledger review passed. The final citation-key consistency correction makes the two BibTeX blocks match.
- `git diff --check` passed. Only the requested local update branch is used; no push or remote branch was created.

The old quotations in this audit are historical evidence, not current-page claims. The reviewer can inspect the local changes and publish after Ali's review.
