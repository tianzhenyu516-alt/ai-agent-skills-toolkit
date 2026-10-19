# Local ESP32-WROOM-32D board-label notes

The author's earlier draft used D/A labels beside GPIO numbers, but it did not identify the carrier board that defines those labels. ESP32-WROOM-32D is a module name, not a universal D-pin labeling scheme. Use this table only to compare against a supplied carrier-board schematic; never treat it as a default pinout.

| Draft board labels | Draft GPIO |
| --- | --- |
| D2, D3, D4, D5, D6, D7 | 25, 26, 27, 0, 14, 13 |
| D8, D9, D10, D11, D12, D13 | 5, 2, 17, 16, 4, 12 |
| A0, A1, A2, A3, A4 | 36/37, 38/39, 34, 35, 15 |
| TX, RX | 1, 3 |

Confirm the exact board's silk-screen labels, electrical limitations, input-only pins, boot strapping, and peripheral multiplexing before using any row.
