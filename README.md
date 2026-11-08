# SpendWise Privacy Policy

This repository contains the public privacy policy for SpendWise.

- Privacy policy: [PRIVACY_POLICY.md](PRIVACY_POLICY.md)
- Web version: https://sudarshanchaudhari.github.io/spendwise-privacy-policy/
- Contact: sunny.sudarshan@gmail.com

## The nuance not to lose from this policy

SpendWise's permission list on Play includes `INTERNET`, but no SpendWise feature uses the network. It is declared by `com.google.android.datatransport:transport-backend-cct`, pulled in transitively by Google's ML Kit text-recognition library, whose receipt-scanning feature is not reachable in this build.

Any future edit must keep that explanation. Dropping it leaves a finance app that appears to have network access with no account of why.

## Editing

`PRIVACY_POLICY.md` is the source of truth. `index.html` carries the same content for GitHub Pages and must be updated in the same commit — Pages serves `main` at the repository root with no build step, so a change to the Markdown alone does not reach the published page.

The copy in the [SpendWise app repository](https://github.com/SUDARSHANCHAUDHARI/SpendWise/blob/main/PRIVACY_POLICY.md) is kept identical to this one.

This README no longer duplicates the policy text. It used to, which left three copies of the same document drifting apart.
