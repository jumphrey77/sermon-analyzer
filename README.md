# Sermon Analyzer

## Purpose

Sermon Analyzer is a config-driven sermon processing system designed to ingest sermon media, transcribe it, analyze structure and references, compare content against doctrinal expectations, and generate structured outputs such as transcripts, church notes, outlines, and reports.

## Project Goals

* Build one shared sermon processor with no duplicated core logic
* Support single-sermon, historical backfill, and ongoing scheduled processing
* Keep outputs deterministic and version-aware
* Support future book-generation workflows from sermon content

## Current Architecture

### Workflows

* Config Intake
* Historical Backfill
* Scheduled Discovery
* Single Sermon
* Shared Sermon Processor

### Core Processing Stages

* Ingestion
* Transcription
* Analysis
* Output Generation
* State Update

## Content Classifications

* SERVICE
* SCRIPTURE_READING
* SERMON
* BENEDICTION

## Sermon Feature Tags

* HUMOR
* SARCASM
* ANALOGY
* CURRENT_EVENT
* BIBLICAL_EVENT
* POLITICAL_EVENT
* NATURAL_DISASTER

## Repo Structure

docs/ \n prompts/ \n workflow/ \n config/ \n registry/

## MVP Rules

* JSON config is the canonical workflow input
* Backfill uses explicit sermon list
* Rerun strategy is full rerun only
* Track workflow version and prompt bundle version
* No duplicated core logic

## How to Work in This Repo

* JSON = machine truth
* Markdown = human docs
* Small updates only
* Version everything important

## Next Steps

* Build n8n shared processor
* Add registry + prompt bundle
* Define data contracts
* Implement discovery + outputs


