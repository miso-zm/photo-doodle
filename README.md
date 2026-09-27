# Daily Line

A Codex skill for turning everyday photos into sparse hand-drawn line illustrations. It preserves the photographed people, pets, clothing, poses, relationships, and recognizable colors while simplifying the background and details.

## Install

Clone this repository into your Codex skills directory as `photo-doodle`:

```sh
git clone https://github.com/miso-zm/photo-doodle.git ~/.codex/skills/photo-doodle
```

Then ask Codex to use `photo-doodle` with an uploaded photo. The skill uses the available image-generation tool and the included style anchors.

## What's included

- `SKILL.md`: workflow, visual rules, and prompt skeleton.
- `references/`: detailed style rules, photo-type guidance, and quality checks.
- `assets/`: four style anchors for overall composition, full-body color, line weight, and face/line/fill simplification.
- `agents/openai.yaml`: display metadata.

The public package uses the included generated anchors. Two external inspiration images used during development are not redistributed because their publication rights have not been established.
