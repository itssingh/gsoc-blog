Title: Coding Period Week-8
Date: 2021-07-27
Category: Coding Period
Tags: coding-period, week-7, gsoc-21, fossology, scancode
Author: Sarita Singh
Summary: This is the eighth week meeting during coding period.


### Attendees 

- [Michael C. Jaeger](https://github.com/mcjaeger)
- [Gaurav Mishra](https://github.com/GMishx)
- [Avinal Kumar](https://github.com/avinal)
- [Sarita Singh](https://github.com/itssingh)

### Week 7 Progress

- Added boost `program_options` library to get scan flags.
- Changed state class of ScanCode agent to include `cliOptions` along with `agentId`.
- Upload from `VCS` is working now for ScanCode and other `parameterize` agents.
- Working upon email/url/author tabs `cookies`, they are not working as expected.
- Added parameters for ScanCode Toolkit in the upload section.

    ![image](images/upload_file.png)

- Flags are inserted in the `jobqueue` table under `jq_cmd_args`.
- Upload from version control is not working for ScanCode with new parameters.

### Discussions

- Under Email/URL/Author bulk view, sticky tabs are not working correctly.
    - Whenever we refresh the page, active tab according to cookies is not sync with UI.
    - Gaurav would see the code if it can be fixed.
- `cmd_args` for ScanCode will have prefix as `scan=`
- Upload from VCS have agents schedules in two levels as shown below

    ![image](images/vcs_job.png)

  Gaurav confirmed it to be normal as levels of schedules depends on the scheduler working.
- scheduleAgents function in php code has 

### Conclusion and Further Plans

- Add ScanCode in copyright single file view along with FOSSology copyright agent.
- There would be two sticky tabs each for ScanCode and FOSSology in the single file view under scanners findings.
- Fix schedule tabs for ScanCode and FOSSology

    ![image](images/schedule.png)


## Coding Week 8 Meeting 2
`Date:2021-07-31`

### Attendees 

- [Gaurav Mishra](https://github.com/GMishx)
- [Anupam Ghosh](https://github.com/ag4ums)
- [Avinal Kumar](https://github.com/avinal)
- [Sarita Singh](https://github.com/itssingh)


### Discussions

- List of tasks remains:
    - Minimum score fix to 50
    - Error handling in ScanCode
    - URL tabs fix
    - Installation script for ScanCode
    - Initial PR for integrating ScanCode-Toolkit to FOSSology
    - Custom template PR(ScanCode toolkit project)
    - Create a ScanCode plugin to get license text
    - Copyright agent schedule
    - code refactoring
    - Write tests for scancode agent
    - Copyright Highlight
    - Complete CLI for scancode agent
    - Integrate scancode copyright in the report 

### Conclusion and Further Plans

- This list of tasks are according to priority
- complete first four tasks and raise an initial pr ASAP
- It would be easier to review code with pr and suggest changes needed