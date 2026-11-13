# Software architecture (planned, not implemented)

## Processing pipeline
1. **capture** — get a still image from Camera Module 3 using Picamera2.
2. **scene** — describe visible objects/relationships; do not guess identity or unsupported details.
3. **retrieval** — match scene concepts to tagged notes in the chosen personality archive; begin with simple keyword retrieval, add embeddings only if required.
4. **personality** — assemble worldview-specific context, tone, constraints and source notes.
5. **generation** — call a vision/language model or locally available language model; generate 1–2 original sentences.
6. **speech** — text-to-speech with Piper (local) or cloud TTS, played via the tested BrainCraft codec.
7. **controller** — cooldown, duplicate suppression, status, graceful fallback and retry limits.
8. **deployment** — run as a systemd service with restart, bounded logs and clean shutdown.

## Example input/output
```json
{
  "observation": {"objects": ["coffee cup"], "scene": "A cup on a table"},
  "personality": "01_philosopher",
  "knowledge_tags": ["attention", "impermanence"],
  "response": "Even an ordinary cup changes when you truly notice it.",
  "source_type": "original_generated_text"
}
```

## Privacy and service
- Do not retain frames or record audio from visitors by default.
- Never place API keys, Wi-Fi passwords, or personally identifying captures in Git.
- Cloud vision requires connectivity; respond with silence or an explicitly static fallback if unavailable.
- The artist should edit personality and knowledge files without changing camera code.

## Decisions not yet made
Cloud provider/model, offline TTS voice, whether there is motion detection, exact audio driver choice, and source-text licensing.
