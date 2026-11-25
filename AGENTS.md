# Repository Guidelines

## Project Structure & Organization

This repository contains personal Heart Sutra transcription and study records, not application code.

- `心经-YYYYMMDD.md`: daily scripture text followed by that day's lesson.
- `心经抄写原文/`: separate transcription records where already used.
- `心经原文范本.md`: reference scripture text and punctuation.
- `心经学习规则.md`: authoritative daily workflow and teaching requirements.
- `心经学习进度.md`: chronological study history and next passage.
- `AGENTS.md`: shared Claude/Codex instructions and current progress.
- `CLAUDE.md`: imports `AGENTS.md` for Claude compatibility; maintain rules here.
- `README.md`: repository overview.

## Development & Validation Commands

There is no build system, application runtime, dependency installation, or automated test suite. Edit Markdown directly and review it in a Markdown preview.

- `git status --short`: inspect pending changes before editing or staging.
- `git diff -- 心经-20261117.md 心经学习进度.md AGENTS.md`: review a daily update; substitute the relevant date.
- `git diff --check`: check tracked changes for whitespace errors. Preserve intentional Markdown hard breaks in the reference text.
- `git log -5 --oneline`: inspect recent commit conventions.

## Markdown Style & Naming

Use UTF-8 Markdown and Chinese for scripture and lessons. Daily filenames use an eight-digit date, such as `心经-20261118.md`. Keep scripture clauses on separate lines and preserve Chinese punctuation from the reference.

Follow existing lesson headings: `## 今日学习`, the passage as a third-level heading, pinyin, explanations, `经文互证`, `照见自己`, `例子`, and `今日练习`, as relevant. No formatter or linter is configured.

## Content Review Guidelines

Compare the full transcription against `心经原文范本.md`: characters, punctuation, and clause order. Verify citations and distinguish history, legend, and literary examples. Keep the lesson, progress ledger, and `AGENTS.md` consistent. There is no coverage threshold.

## Commit & Pull Request Guidelines

History uses concise `docs:` messages, commonly `docs: continue third Heart Sutra study cycle`. Stage only relevant files. Pull requests should describe the date or passage, corrections, and content checks; no PR template or screenshot requirement is present.

## Agent Workflow

详细规则见：`心经学习规则.md`。完整进度见：`心经学习进度.md`。原文格式见：`心经原文范本.md`。开始学习前先读取这三份文件。

当用户说“新的一天”或开始新的《心经》学习时：

1. 只给用户《般若波罗蜜多心经》原文，方便用户先抄写。
2. 不要立即创建或更新当天文档，也不要展开当天教学。
3. 用户说“抄好了”或表示抄写完成后，先检查当天抄写有没有错字、漏字或明显标点问题。
4. 若用户要求重新检查，必须重新核对全文后再下结论。
5. 确认抄写无误后，再创建或更新当天学习文档，文件名使用 `心经-YYYYMMDD.md`。
6. 再给当天教学内容，并同步写入当天文档。
7. 教学节奏保持慢而稳，每天只学习一句或一个小段。
8. 教学内容和学习进度更新后，自动执行 `git add`、`git commit`、`git push`，无需用户再提醒。

## 当前学习状态

- 当前轮次：第三轮（2026-10-10 开始）
- 第三轮学习方式：继续每天一句或一小段，仍含“照见自己”和小步练习；例子继续优先讲清一个，可跨佛经、历史、文学、科学取材，并分清史实、传说与文学情节。
- 最近已学：`菩提萨埵，`
- 下一次从：`依般若波罗蜜多故，` 开始。
