Title: Coding Period Week-7
Date: 2021-07-20 
Category: Coding Period
Tags: coding-period, week-7, gsoc-21, fossology, scancode
Author: Sarita Singh
Summary: This is the seventh week meeting during coding period.

### Attendees 

- [Michael C. Jaeger](https://github.com/mcjaeger)
- [Gaurav Mishra](https://github.com/GMishx)
- [Anupam Ghosh](https://github.com/ag4ums)
- [Avinal Kumar](https://github.com/avinal)
- [Sarita Singh](https://github.com/itssingh)

### Week 6 Progress

- Populated copyright table for scancode.
- Extended Email/URL/Author Browser to add scan result by ScanCode.
- There are two levels of pagination one for FOSSology and ScanCode and other for email/url/author tabs.

    ![image](images/author.png)

- All the available options for Test replacement, Replace selected rows and, Deactivate selected rows are working good.

### Discussions

- There is a bug in the pagination of the Email/URL/Author Browser. It could be possibly because of cookies. Check out storage of the inspect page, there will be index for different `cookies` and it would be helpful in debugging.
- Maintagent can be taken as a reference to create verbose flags. ScanCode UI will look like reuser/desider in the upload section.
- There is a problem in finding start byte of copyright due to `unicode character`.
- ScanCode change `©` to `(c)` and also removes some of the characters like `:` from `copyright(c): Sarita Singh` and scan results to `copyright (c) Sarita Singh`. This thing causes issue in finding start byte of copyright and also integrating scancode copyright to report(unable to remove redundant data). 
- Michael suggested to drop copyright and `unicode characters` and then use sub-string matching to find approx. position(but it would be inaccurate).
- Creating a ScanCode plugin to get `copyright text` like `matched license text` would solve the issue.

### Conclusion and Further Plans

- Fix author tabs.
- Use verbose flags for scancode agent like maintagent.
- creating a scancode plugin to get copyright text can work. 

## Coding Week 7 Meeting 2
`Date:2021-07-23`

### Attendees 

- [Michael C. Jaeger](https://github.com/mcjaeger)
- [Gaurav Mishra](https://github.com/GMishx)
- [Anupam Ghosh](https://github.com/ag4ums)
- [Shaheem Azmal](https://github.com/shaheemazmalmmd)
- [Avinal Kumar](https://github.com/avinal)
- [Sarita Singh](https://github.com/itssingh)


### Discussions

- ScheduleAgent function code in `scancode/ui/agent_scancode.php` is correct.
- Format of flag for `jq_cmd_args` depends upon the code we are using to parse this flag inside the ScanCode agent.
- Gaurav suggested to take reference for cliOptions from copyright or ojo agent.
- They are using `Boost.Program_options` library which can be used to parse command line arguments and get ScanCode flags.
- Further, this code can be reused for adding ScanCode agent to run by command line.

### Conclusion and Further Plans

- ScheduleAgent function in `scancode/ui/agent_scancode.php`.
- Next step is to parse the scancode args to get scancode CLI flags.
- Use Boost program options for scancode CLI.
