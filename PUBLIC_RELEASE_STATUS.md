# Experimental release status

ReverseShield is an **experimental local static-analysis workbench**. It is not
a production security product, malware sandbox, protection guarantee or
behavioral-equivalence proof.

## Distribution provenance and privacy

This repository starts with a new root commit containing an audited source
snapshot. It does **not** import the development repository's Git history,
branches, pull requests, old reports or old release assets. The starting source
snapshot was development commit
`e05756b0c3240e1abd711967c883d50634036b4c`; this identifier is provenance, not an
additional commit included in the clean repository.

A bounded audit of the starting snapshot and its Lite candidate found no actual
workstation-home/build paths or plausible nonfixture credentials. This is not
an absolute guarantee: detectors and English OCR have limitations. Deliberate
test examples and team attribution remain; they are not credentials.

The private development history contained identifying paths in older documents
and sample binaries, plus personal contact details in commit metadata. That
history must remain private. Do not merge, mirror-push or restore branches from
it into this clean repository. Preserve contributor attribution when making
changes. Review future commits and artifacts before sharing them.

## Experimental platform support

**Clean native-Windows manual setup and UI acceptance remain incomplete.**
Windows CI does not replace testing a clean non-admin account with `setup.bat`,
`run.bat`, ELF/PE analysis, a supported Compare operation and an inspected
sanitized report download. Treat the Lite Windows ZIP as experimental.

The optional OLLVM/QEMU workflow is Linux-only. It compares separate deterministic
sample drivers in a no-disk/no-network guest, not the downloadable protected
ELF. Six sample fixtures can be analyzed statically; only the original five
sources are eligible for source transformations. Selected targets and changed
artifacts are never launched on the host.

## Verification and evidence

The source and freshly extracted Lite candidate are tested before attaching a
release asset. Consult the release's `RELEASE_MANIFEST.json` for the exact clean
commit, archive contents/checksum, measured test results and remaining skips.
Historical results under `docs/evidence/` retain their original date/scope and
must not be represented as a fresh security certification of this distribution.

The release manifest and current test logs, rather than a historical hardcoded
count in a report generator, establish which candidate was exercised. Optional
tool skips and pending manual checks remain visible. Review
`docs/RELEASE_CHECKLIST.md` for operating and sharing limitations.

## License decision

The owner has left the project license **pending**. No MIT or other project-wide
license is granted by this status document. Do not describe this release as
MIT-licensed or assume broad reuse/redistribution permission. Third-party
components retain their own terms; see `THIRD_PARTY_NOTICES.md`. A license can
be added later with authorization from the relevant contributors.

## Before publishing

Publication and repository visibility require explicit owner approval. Keep the
release labeled **Experimental / prerelease**, state the native-Windows manual
acceptance limitation, and publish only the verified source candidate and its
matching checksum/manifest. Do not upload private audit outputs, raw analysis
runs, credentials, downloaded tool bundles or old development release ZIPs.
