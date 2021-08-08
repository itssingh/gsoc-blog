Title: Coding Period Week-6
Date: 2021-07-13 
Category: Coding Period
Tags: coding-period, week-6, gsoc-21, fossology, scancode
Author: Sarita Singh
Summary: This is the sixth week meeting during coding period.


### Attendees 

- [Michael C. Jaeger](https://github.com/mcjaeger)
- [Gaurav Mishra](https://github.com/GMishx)
- [Avinal Kumar](https://github.com/avinal)
- [Sarita Singh](https://github.com/itssingh)


### Week 5 Progress

- Added ScanCodeFindings table in Copyright Browser on UI.
- Working on populating this table with scancode_copyright data.
- Created tables for `scancode_copyright_event` and `scancode_author_event`.
- Added copyright and license text in source code.
- Added comments for source code.
- Merged `LicenseMatch` to `Match` class
- Instead of using `vector` of `LicenseMatch` class, using `map` of type Match class in `scancode_wrapper` to save parsed value of result scanned by ScanCode.

### Discussions

- Instead of using RuleBits as done by decider, using flags as scancode CLI options conventions would be nice.
- These could be various flags:
    - -l -> license
    - -c -> copyright and holder
    - -e -> email in the file, and
    - -u -> URL in the file
- These flags would be used in [ScanCode command](https://github.com/itssingh/fossology/blob/feat/newagent/scancode-toolkit/src/scancode/agent/scancode_wrapper.cc#L76).
- Gaurav suggested to look for [Maintagent UI](https://github.com/fossology/fossology/blob/master/src/maintagent/ui/maintagent.php#L86). It uses flags ( more verbose ).
- It would be nice to implement ScanCode for CLI, can do this after once done with copyright/author UI.

### Conclusion and Further Plans

- Add flags for ScanCode command to keep it verbose and match with scancode CLI flags.
- Try to complete copyright UI by next meet.
- Next task would be to implement ScanCode for CLI options once done with copyright/author UI.