# Power Automate Working Hours Condition

This project provides a solution for executing actions within a specified time range (08:00 - 17:00) using Microsoft Power Automate. The primary goal is to ensure that certain workflows are triggered only during standard business hours. The solution utilizes a time-based condition that can be integrated seamlessly into your Power Automate flows.

## How It Works

1. The Power Automate flow is initiated by a trigger, such as a scheduled time or an event.
2. A condition is used to check if the current time falls within the specified working hours (08:00 - 17:00 GMT).
3. If the condition is met, the flow continues to execute the designated actions.
4. If the condition is not met, the flow either halts or redirects to an alternative path, ensuring that the workflow only operates during the desired time range.

   
## Features

- Time-based Condition: Execute actions only during predefined working hours.
- Adaptable Time Zones: Easily modify the condition to work with different time zones according to your needs.
- Efficient Workflow Management: Prevents workflows from running outside of business hours, ensuring better resource management.
- Seamless Integration: Compatible with various Power Automate triggers and actions.

## Requirements

- Microsoft Power Automate subscription
- Basic understanding of Power Automate flow creation

## Getting Started

1. Import the provided condition formula into your Power Automate flow.
2. Adjust the time zone and working hours if necessary to match your organization's requirements.
3. Integrate the condition into your workflow to ensure actions are only executed during the specified time range.

Formula

```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Turkey Standard Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Turkey Standard Time'), 'HH')), 18))
```

This formula checks if the current time is between 08:00 and 17:00 in the GMT time zone and proceeds with the workflow if the condition is true.


United States (Eastern Standard Time)
```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Eastern Standard Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Eastern Standard Time'), 'HH')), 18))
```
United Kingdom (Greenwich Mean Time)
```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'GMT Standard Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'GMT Standard Time'), 'HH')), 18))
```
France (Central European Time)
```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Central European Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Central European Time'), 'HH')), 18))
```
Germany (Central European Time)
```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Central European Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'Central European Time'), 'HH')), 18))
```
Australia (Australian Eastern Standard Time)
```plaintext
and(greaterOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'AUS Eastern Standard Time'), 'HH')), 8), lessOrEquals(int(formatDateTime(convertTimeZone(utcNow(), 'UTC', 'AUS Eastern Standard Time'), 'HH')), 18))
```
![Example Condition](https://github.com/korhanh/power-automate-time-condition/blob/main/Example-Condition.PNG)



## Contributions and Feedback

Contributions to this project are welcome! If you encounter any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](https://github.com/korhanh/power-automate-time-condition/blob/main/LICENSE).

Feel free to use, modify, and distribute this project according to the terms specified in the license.

## Credits

This project is created and maintained by [korhanh]([link_to_your_github_profile](https://github.com/korhanh)).

If you use this project or find it helpful, consider giving it a star on GitHub!

Happy PDF page splitting! :rocket:
