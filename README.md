# YANG 2 and friends

This is the repository for four documents:
  - `draft-yn-netmod-yang-2`: The YANG 2.0 Data Modeling Language
  - `draft-yn-netmod-yang-xml`: XML Encoding of Data Modeled with YANG
  - `draft-yn-netmod-yang-proto`: Requirements for YANG-based Protocols
  - `draft-yn-netconf-netconf-2`: Placeholder text for NETCONF-next.

The first document is primary, the other documents are the "friends" ;)

All documents are in the same repository so that a single GitHub pull
request (PR) can update them together.

The initial goal is to make the document not be XML or NETCONF specific,
thus setting a baseline for subsequent changes.  This is accomplished by:
  - removing the "XML Encoding" sections.
  - removing the "NETCONF &ltl;edit-config&gt; Operations" sections.
  - removing the "NETCONF XML Encoding Rules" sections.
  - removing the "Example Usage" sections.
  - making remaining examples be both XML and JSON.

XML-specific text moves to the new `yang-xml` document, which is
modeled after RFC 7951 (JSON Encoding of Data Modeled with YANG).

NETCONF-specific text moves to the `netconf-2` document, which is
expected to be considered by the NETCONF WG to update RFC 6241.



## Build Artifacts and Diffs

https://netmod-wg.github.io/yang2-and-friends

GitHub workflow actions are used to automatically build, test, and
publish the three drafts, in the `html`, `txt`, and `xml` formats.
This automation occur for both the `main` branch and every PR-branch.

The webpage also provide links to:
  - diff a PR-branch against the `main` branch.
  - diff the `main` branch against Datatracker.
  - for yang2 only, diff `main` against RFC 7950.


## Contributing

All contributions are made using pull requests (PRs).

Please see the [contributing](https://github.com/netmod-wg/yang2-and-friends/blob/main/CONTRIBUTING.md) page for details.


## Command Line Usage

Formatted text and HTML versions of the draft can be built using `make`.

```sh
$ make clean && make
```

Command line usage requires that you have the necessary software installed.
You will need `make`, `python`, `xml2rfc`, and `rfcfold`.
