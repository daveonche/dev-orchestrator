# Environment Adaptations

The core loop (draft → test → review → improve → repeat) is the same
everywhere; the mechanics change by environment.

## Claude.ai

- No subagents: run test cases yourself, one at a time, following
  the skill's SKILL.md for each prompt. Less rigorous (you wrote the
  skill and you're running it), but a useful sanity check; the human
  review step compensates.
- Skip baseline runs and quantitative benchmarking — baselines are
  meaningless without subagents; rely on qualitative feedback.
- No browser/display: skip the browser viewer; present prompt and
  output inline per test case. Save output files the user needs
  (e.g., .docx, .xlsx) to the filesystem and say where they are.
- Description optimization needs the `claude` CLI (`claude -p`) —
  skip it.
- Blind comparison needs subagents — skip it.
- Packaging works: run the packaging script; the user downloads the
  resulting `.skill` file.

## Cowork

- Subagents work; on severe timeouts, run test prompts in series.
- No browser/display: generate the eval viewer with `--static
  <output_path>` as a standalone HTML file and proffer the link.
- Always generate the eval viewer before evaluating outputs yourself
  — get examples in front of the human first.
- Feedback: the viewer's submit button downloads `feedback.json`;
  read it from the download (requesting access if needed).
- Packaging works (Python + filesystem).
- Description optimization works (it shells out to `claude -p`) —
  but run it only after the skill is finished and the user agrees
  it's in good shape.

## Updating an installed skill

- Preserve the original name: keep the directory name and `name`
  frontmatter unchanged, and package under the same name (not
  `-v2`).
- The installed path may be read-only: copy to a writable location
  (e.g., `/tmp/<skill-name>/`) before editing.
- When packaging manually, stage in `/tmp/` first, then copy to the
  output directory — direct writes may fail on permissions.

## Packaging

Package a skill folder into a `.skill` archive with the upstream
packaging script (see the pack Source note), then direct the user to
the resulting file path.
