# countdown
A countdown timer built with HTML, CSS, and JavaScript. It displays the remaining time, using your device's current time as the reference.

## Usage

1. Download the files from the repository;
2. Open the HTML file in your browser (with JavaScript support);
3. Specify the parameters.

## URL parameters
| Parameter | Aliases | Type | Default | Description |
| --- | --- | --- | --- | --- |
| `date` | `target`, `end` | string | `2026-06-13T19:00:00` | Target date and time. Format: `YYYY-MM-DDTHH:MM:SS` (local time). |
| `name`| `title` | string | `Countdown` | Text shown in the tab title. |
| `timesup` | `timesUp`, `endText` | string | `Time's up` | Text shown when the countdown reaches zero. |
| `format` |  | `1`, `2`, `3` or `4` | `1` | The format used to display the target date. `1`: `MM/DD/YYYY HH:MM:SS`; `2`: `DD/MM/YYYY HH:MM:SS`; `3`: `DD.MM.YYYY HH:MM:SS`; `4`: `DD-MM-YYYY HH:MM:SS`. |
| `backgroundcolor` | `bgc`, `background` | hex | `#fff` | Background color. |
| `maincolor` | `mc`, `main` | hex | `#000` | Main countdown text color. |
| `targetdatecolor` | `tdc`, `targetcolor` | hex | `#7f7f7f` | Target date text color. |
| `dark` |  | `true`, `false`, `1` or empty |  | **Deprecated.** If used, it automatically converts to `backgroundcolor=000`, `maincolor=fff`, `targetdatecolor=a0a0a0`. |

Examples:
| Link | Date | Tab title | Time's up text | Target date format | Colors |
| --- | --- | --- | --- | --- | --- |
| index.html?dark=1&format=3&name=2027&date=2027-01-01T00:00:00&timesup=Happy%20new%20year! | `Year: 2027; month: January; day: 1; hour: 0; minute: 0; second: 0.` | `2027` | `Happy new year!` | `DD.MM.YYYY HH:MM:SS` | Background color: `#000000`; main color: `#ffffff`; target date color: `#a0a0a0` |
| index.html?format=2&name=Vacation&date=2027-07-15T12:00:00 | `Year: 2027; month: July; day: 15; hour: 12; minute: 0; second: 0.` | `Vacation` | `Time's up` (Default) | `DD/MM/YYYY HH:MM:SS` | Background color: `#ffffff`; main color: `#000000`; target date color: `#7f7f7f` (Default) |
| index.html?timesup=Abcdef&name=Example&backgroundcolor=111&maincolor=eee&targetdatecolor=999 | `Year: 2026; month: June; day: 13; hour: 19; minute: 0; second: 0.` (Default) | `Example` | `Abcdef` | `MM/DD/YYYY HH:MM:SS` (Default) | Background color: `#111111`; main color: `#eeeeee`; target date color: `#999999` |
| `index.html?timesup=Almost%20there&dark&name=test` | `Year: 2026; month: June; day: 13; hour: 19; minute: 0; second: 0.` (Default) | `test` | `Almost there` | `MM/DD/YYYY HH:MM:SS` (Default) | Background color: `#000000`; main color: `#ffffff`; target date color: `#a0a0a0` |
