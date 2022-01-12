# GIT TAGS

- Git tags are labels that refer to specific commits in the history
- These are usually used to label/mark somekind of version of the project
- Can also be said as branch references that do not change
- Two types of tags -

  1. **Lightweight** - These are simply a label to a new commit

  2. **Annotated** - These have a small message kinda like commit messages and also contain the author name, email etc. Just stores some metadata about the tag

## SEMANTIC VERSIONING

- It is the typical versioning of a software which is standardized.
- Provides a consistent way for devs to give meaning to their software releases
- Consists of 3 numbers seperated by periods like **_a.b.c_**

- Now a.b.c have specific meanings -

  - a - Major release (Significant releases that are not backwards compatible. There are features that might be removed or changed a lot. The other 2 numbers are set back to zero)
  - b - Minor release (New features and functionality but the code is still backwards compatible. The users must not be forced to rewrite their own code. No breaking changes. Whenever there is a minor release, the patch release is set to 0 again)
  - c - Patch release (Simple Bug fixes and code fixes that have no major impact)

- The very first version that is released (public API) is versioned as 1.0.0
