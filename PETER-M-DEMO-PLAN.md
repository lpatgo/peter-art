---
name: Peter M Demo Launch
overview: Review and refresh Peter M’s static site by adding new images to the top of the Student Work page, publish a demo build to a SiteGround subfolder, and prepare a clean path to final deployment on CeilingSky.
todos:
  - id: collect-baseline
    content: Create local baseline snapshot and identify Student Work image block
    status: pending
  - id: prepare-images
    content: Optimize and rename new student images consistently
    status: pending
  - id: implement-studentwork
    content: Insert new image entries at top of Student Work markup with alt text
    status: pending
  - id: demo-deploy-siteground
    content: Upload updated site to SiteGround demo subfolder and validate paths
    status: pending
  - id: feedback-and-finalize
    content: Iterate on client feedback and prepare final CeilingSky deployment package
    status: pending
isProject: false
---

# Peter M Demo Launch Plan

## Goal

Get a clean demo online quickly for client review, then preserve a low-risk path to final deployment on CeilingSky with SSL.

## Scope

- Source: local static HTML/CSS/JS project copy
- Content change: add new images at the top of the Student Work page
- Demo target: subfolder on your SiteGround-hosted site
- Final target (later): CeilingSky host for petermandradjieff.net

## Phase 1: Baseline capture and project review

- Download/collect a full local working copy of the current project (including `images/`, CSS, JS, and page files).
- Create a dated project snapshot folder before changes (for rollback).
- Open the Student Work page and identify:
  - the container/block where current student images are rendered,
  - image path pattern and naming convention,
  - whether layout is plain HTML, CSS grid/flex, or JS-assisted.
- Build a short review checklist while scanning site-wide:
  - broken links, missing images, mobile layout issues, and obvious legacy copy.

## Phase 2: Add new student images (top of Student Work)

- Prepare images before insertion:
  - normalize filenames (`student-work-01.jpg`, etc.),
  - resize to consistent display dimensions,
  - export web-friendly formats (`.jpg`/`.webp`) and reasonable file sizes.
- Add image files into the existing images directory used by Student Work.
- Insert new image markup at the top of the Student Work section while preserving existing structure/classes.
- Add/update `alt` text for each image (brief, descriptive, non-keyword-stuffed).
- Verify in browser at desktop + mobile widths:
  - loading order (new images appear first),
  - spacing/alignment consistency,
  - no overflow or broken thumbnails.

## Phase 3: Demo deployment to SiteGround subfolder

- Create a dedicated subfolder for demo (example: `/public_html/peterm-demo/`).
- Upload the full updated static site into that folder via SiteGround File Manager or SFTP.
- Validate URLs and relative paths in the subfolder context:
  - images, CSS, JS load correctly,
  - no root-relative path breaks (e.g., `/images/...` may need adjustment if used).
- Smoke test demo link end-to-end and share with Peter for review.

## Phase 4: Approval loop and launch readiness

- Collect Peter’s feedback in one round of tracked notes.
- Apply revisions locally first, then re-upload to the same demo subfolder.
- Keep a simple changelog of edits between demo versions.

## Phase 5: Final migration to CeilingSky (post-approval)

- Package final approved site build.
- Deploy to CeilingSky document root for the final domain.
- Enable SSL and force HTTPS redirect.
- Run post-launch verification:
  - homepage + Student Work + contact links,
  - image loading/performance,
  - redirect and certificate validity.

## Risk controls

- Keep untouched backup of original project and each deployment milestone.
- Avoid editing only-in-production files; treat local copy as source of truth.
- Use a fixed demo folder name to avoid link churn while client reviews.

## Deliverables

- Updated local project with new Student Work images at top
- Working demo URL in SiteGround subfolder
- Final deploy-ready package for CeilingSky migration

