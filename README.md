# Predicitng-Salary-Using-Linear-Regression
The data set is from 
https://www.kaggle.com/datasets/rsadiq/salary



[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)



[![forthebadge](data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIzMjcuNDA5OTk5OTk5OTk5OTciIGhlaWdodD0iMzUiIHZpZXdCb3g9IjAgMCAzMjcuNDA5OTk5OTk5OTk5OTcgMzUiPjxyZWN0IGNsYXNzPSJzdmdfX3JlY3QiIHg9IjAiIHk9IjAiIHdpZHRoPSIxMTUuMzEiIGhlaWdodD0iMzUiIGZpbGw9IiMzMUM0RjMiLz48cmVjdCBjbGFzcz0ic3ZnX19yZWN0IiB4PSIxMTMuMzEiIHk9IjAiIHdpZHRoPSIyMTQuMDk5OTk5OTk5OTk5OTciIGhlaWdodD0iMzUiIGZpbGw9IiMzODlBRDUiLz48cGF0aCBjbGFzcz0ic3ZnX190ZXh0IiBkPSJNMTUuNjkgMjJMMTQuMjIgMjJMMTQuMjIgMTMuNDdMMTYuMTQgMTMuNDdMMTguNjAgMjAuMDFMMjEuMDYgMTMuNDdMMjIuOTcgMTMuNDdMMjIuOTcgMjJMMjEuNDkgMjJMMjEuNDkgMTkuMTlMMjEuNjQgMTUuNDNMMTkuMTIgMjJMMTguMDYgMjJMMTUuNTUgMTUuNDNMMTUuNjkgMTkuMTlMMTUuNjkgMjJaTTI4LjQ5IDIyTDI2Ljk1IDIyTDMwLjE3IDEzLjQ3TDMxLjUwIDEzLjQ3TDM0LjczIDIyTDMzLjE4IDIyTDMyLjQ5IDIwLjAxTDI5LjE4IDIwLjAxTDI4LjQ5IDIyWk0zMC44MyAxNS4yOEwyOS42MCAxOC44MkwzMi4wNyAxOC44MkwzMC44MyAxNS4yOFpNNDEuMTQgMjJMMzguNjkgMjJMMzguNjkgMTMuNDdMNDEuMjEgMTMuNDdRNDIuMzQgMTMuNDcgNDMuMjEgMTMuOTdRNDQuMDkgMTQuNDggNDQuNTcgMTUuNDBRNDUuMDUgMTYuMzMgNDUuMDUgMTcuNTJMNDUuMDUgMTcuNTJMNDUuMDUgMTcuOTVRNDUuMDUgMTkuMTYgNDQuNTcgMjAuMDhRNDQuMDggMjEuMDAgNDMuMTkgMjEuNTBRNDIuMzAgMjIgNDEuMTQgMjJMNDEuMTQgMjJaTTQwLjE3IDE0LjY2TDQwLjE3IDIwLjgyTDQxLjE0IDIwLjgyUTQyLjMwIDIwLjgyIDQyLjkzIDIwLjA5UTQzLjU1IDE5LjM2IDQzLjU2IDE3Ljk5TDQzLjU2IDE3Ljk5TDQzLjU2IDE3LjUyUTQzLjU2IDE2LjEzIDQyLjk2IDE1LjQwUTQyLjM1IDE0LjY2IDQxLjIxIDE0LjY2TDQxLjIxIDE0LjY2TDQwLjE3IDE0LjY2Wk01NS4wOSAyMkw0OS41MSAyMkw0OS41MSAxMy40N0w1NS4wNSAxMy40N0w1NS4wNSAxNC42Nkw1MS4wMCAxNC42Nkw1MS4wMCAxNy4wMkw1NC41MCAxNy4wMkw1NC41MCAxOC4xOUw1MS4wMCAxOC4xOUw1MS4wMCAyMC44Mkw1NS4wOSAyMC44Mkw1NS4wOSAyMlpNNjYuNjUgMjJMNjQuNjggMTMuNDdMNjYuMTUgMTMuNDdMNjcuNDcgMTkuODhMNjkuMTAgMTMuNDdMNzAuMzQgMTMuNDdMNzEuOTYgMTkuODlMNzMuMjcgMTMuNDdMNzQuNzQgMTMuNDdMNzIuNzcgMjJMNzEuMzUgMjJMNjkuNzMgMTUuNzdMNjguMDcgMjJMNjYuNjUgMjJaTTgwLjM4IDIyTDc4LjkwIDIyTDc4LjkwIDEzLjQ3TDgwLjM4IDEzLjQ3TDgwLjM4IDIyWk04Ni44NyAxNC42Nkw4NC4yMyAxNC42Nkw4NC4yMyAxMy40N0w5MS4wMCAxMy40N0w5MS4wMCAxNC42Nkw4OC4zNCAxNC42Nkw4OC4zNCAyMkw4Ni44NyAyMkw4Ni44NyAxNC42NlpNOTYuMjQgMjJMOTQuNzUgMjJMOTQuNzUgMTMuNDdMOTYuMjQgMTMuNDdMOTYuMjQgMTcuMDJMMTAwLjA1IDE3LjAyTDEwMC4wNSAxMy40N0wxMDEuNTMgMTMuNDdMMTAxLjUzIDIyTDEwMC4wNSAyMkwxMDAuMDUgMTguMjFMOTYuMjQgMTguMjFMOTYuMjQgMjJaIiBmaWxsPSIjRkZGRkZGIi8+PHBhdGggY2xhc3M9InN2Z19fdGV4dCIgZD0iTTEyNi40MiAyMC45M0wxMjYuNDIgMjAuOTNMMTI3LjcxIDE5LjQwUTEyOC4zOCAyMC4yNyAxMjkuMTYgMjAuMjdMMTI5LjE2IDIwLjI3UTEyOS4xNiAyMC4yNyAxMjkuMTcgMjAuMjdMMTI5LjE3IDIwLjI3UTEyOS42OCAyMC4yNyAxMjkuOTUgMTkuOTZRMTMwLjIyIDE5LjY1IDEzMC4yMiAxOS4wNUwxMzAuMjIgMTkuMDVMMTMwLjIyIDE1LjQ0TDEyNy4zMiAxNS40NEwxMjcuMzIgMTMuNjBMMTMyLjU4IDEzLjYwTDEzMi41OCAxOC45MVExMzIuNTggMjAuNTQgMTMxLjc1IDIxLjM2UTEzMC45MyAyMi4xNyAxMjkuMzQgMjIuMTdMMTI5LjM0IDIyLjE3UTEyOC40MSAyMi4xNyAxMjcuNjYgMjEuODVRMTI2LjkwIDIxLjUzIDEyNi40MiAyMC45M1pNMTM3LjU5IDE4LjI2TDEzNy41OSAxOC4yNkwxMzcuNTkgMTMuNjBMMTM5Ljk3IDEzLjYwTDEzOS45NyAxOC4xOVExMzkuOTcgMjAuMjAgMTQxLjU3IDIwLjIwTDE0MS41NyAyMC4yMFExNDMuMTUgMjAuMjAgMTQzLjE1IDE4LjE5TDE0My4xNSAxOC4xOUwxNDMuMTUgMTMuNjBMMTQ1LjQ5IDEzLjYwTDE0NS40OSAxOC4yNlExNDUuNDkgMjAuMTMgMTQ0LjQ1IDIxLjE1UTE0My40MSAyMi4xNyAxNDEuNTQgMjIuMTdMMTQxLjU0IDIyLjE3UTEzOS42NyAyMi4xNyAxMzguNjMgMjEuMTVRMTM3LjU5IDIwLjEzIDEzNy41OSAxOC4yNlpNMTUyLjk2IDIyTDE1MC41OCAyMkwxNTAuNTggMTMuNjBMMTU0LjQyIDEzLjYwUTE1NS41NiAxMy42MCAxNTYuNDAgMTMuOThRMTU3LjI0IDE0LjM1IDE1Ny43MCAxNS4wNlExNTguMTUgMTUuNzYgMTU4LjE1IDE2LjcxTDE1OC4xNSAxNi43MVExNTguMTUgMTcuNjYgMTU3LjcwIDE4LjM1UTE1Ny4yNCAxOS4wNSAxNTYuNDAgMTkuNDJRMTU1LjU2IDE5LjgwIDE1NC40MiAxOS44MEwxNTQuNDIgMTkuODBMMTUyLjk2IDE5LjgwTDE1Mi45NiAyMlpNMTUyLjk2IDE1LjQ3TDE1Mi45NiAxNy45M0wxNTQuMjggMTcuOTNRMTU1LjAxIDE3LjkzIDE1NS4zOCAxNy42MVExNTUuNzUgMTcuMjkgMTU1Ljc1IDE2LjcxTDE1NS43NSAxNi43MVExNTUuNzUgMTYuMTIgMTU1LjM4IDE1LjgwUTE1NS4wMSAxNS40NyAxNTQuMjggMTUuNDdMMTU0LjI4IDE1LjQ3TDE1Mi45NiAxNS40N1pNMTY1LjAzIDE4Ljk1TDE2MS44MyAxMy42MEwxNjQuMzQgMTMuNjBMMTY2LjMzIDE2Ljk0TDE2OC4zMiAxMy42MEwxNzAuNjIgMTMuNjBMMTY3LjQxIDE4Ljk5TDE2Ny40MSAyMkwxNjUuMDMgMjJMMTY1LjAzIDE4Ljk1Wk0xNzYuNTAgMTUuNDhMMTczLjkyIDE1LjQ4TDE3My45MiAxMy42MEwxODEuNDQgMTMuNjBMMTgxLjQ0IDE1LjQ4TDE3OC44NyAxNS40OEwxNzguODcgMjJMMTc2LjUwIDIyTDE3Ni41MCAxNS40OFpNMTkyLjU1IDIyTDE4NS44MSAyMkwxODUuODEgMTMuNjBMMTkyLjQwIDEzLjYwTDE5Mi40MCAxNS40NEwxODguMTcgMTUuNDRMMTg4LjE3IDE2Ljg1TDE5MS45MCAxNi44NUwxOTEuOTAgMTguNjNMMTg4LjE3IDE4LjYzTDE4OC4xNyAyMC4xN0wxOTIuNTUgMjAuMTdMMTkyLjU1IDIyWk0xOTkuNzQgMjJMMTk3LjM2IDIyTDE5Ny4zNiAxMy42MEwyMDEuMjAgMTMuNjBRMjAyLjM1IDEzLjYwIDIwMy4xOCAxMy45OFEyMDQuMDIgMTQuMzUgMjA0LjQ4IDE1LjA2UTIwNC45NCAxNS43NiAyMDQuOTQgMTYuNzFMMjA0Ljk0IDE2LjcxUTIwNC45NCAxNy42MiAyMDQuNTEgMTguMzBRMjA0LjA4IDE4Ljk4IDIwMy4yOSAxOS4zNkwyMDMuMjkgMTkuMzZMMjA1LjEwIDIyTDIwMi41NiAyMkwyMDEuMDMgMTkuNzdMMTk5Ljc0IDE5Ljc3TDE5OS43NCAyMlpNMTk5Ljc0IDE1LjQ3TDE5OS43NCAxNy45M0wyMDEuMDYgMTcuOTNRMjAxLjc5IDE3LjkzIDIwMi4xNiAxNy42MVEyMDIuNTMgMTcuMjkgMjAyLjUzIDE2LjcxTDIwMi41MyAxNi43MVEyMDIuNTMgMTYuMTIgMjAyLjE2IDE1Ljc5UTIwMS43OSAxNS40NyAyMDEuMDYgMTUuNDdMMjAxLjA2IDE1LjQ3TDE5OS43NCAxNS40N1pNMjE5LjAzIDIyTDIxNi43MCAyMkwyMTYuNzAgMTMuNjBMMjE4LjY1IDEzLjYwTDIyMi4zNiAxOC4wN0wyMjIuMzYgMTMuNjBMMjI0LjY5IDEzLjYwTDIyNC42OSAyMkwyMjIuNzQgMjJMMjE5LjAzIDE3LjUyTDIxOS4wMyAyMlpNMjI5LjQyIDE3LjgwTDIyOS40MiAxNy44MFEyMjkuNDIgMTYuNTUgMjMwLjAzIDE1LjU1UTIzMC42MyAxNC41NiAyMzEuNjkgMTQuMDBRMjMyLjc2IDEzLjQzIDIzNC4wOSAxMy40M0wyMzQuMDkgMTMuNDNRMjM1LjQyIDEzLjQzIDIzNi40OCAxNC4wMFEyMzcuNTQgMTQuNTYgMjM4LjE1IDE1LjU1UTIzOC43NiAxNi41NSAyMzguNzYgMTcuODBMMjM4Ljc2IDE3LjgwUTIzOC43NiAxOS4wNSAyMzguMTUgMjAuMDRRMjM3LjU0IDIxLjA0IDIzNi40OCAyMS42MFEyMzUuNDIgMjIuMTcgMjM0LjA5IDIyLjE3TDIzNC4wOSAyMi4xN1EyMzIuNzYgMjIuMTcgMjMxLjY5IDIxLjYwUTIzMC42MyAyMS4wNCAyMzAuMDMgMjAuMDRRMjI5LjQyIDE5LjA1IDIyOS40MiAxNy44MFpNMjMxLjgyIDE3LjgwTDIzMS44MiAxNy44MFEyMzEuODIgMTguNTEgMjMyLjEyIDE5LjA1UTIzMi40MiAxOS42MCAyMzIuOTQgMTkuOTBRMjMzLjQ1IDIwLjIwIDIzNC4wOSAyMC4yMEwyMzQuMDkgMjAuMjBRMjM0LjcyIDIwLjIwIDIzNS4yNCAxOS45MFEyMzUuNzYgMTkuNjAgMjM2LjA1IDE5LjA1UTIzNi4zNSAxOC41MSAyMzYuMzUgMTcuODBMMjM2LjM1IDE3LjgwUTIzNi4zNSAxNy4wOSAyMzYuMDUgMTYuNTRRMjM1Ljc2IDE2IDIzNS4yNCAxNS43MFEyMzQuNzIgMTUuNDAgMjM0LjA5IDE1LjQwTDIzNC4wOSAxNS40MFEyMzMuNDUgMTUuNDAgMjMyLjkzIDE1LjcwUTIzMi40MiAxNiAyMzIuMTIgMTYuNTRRMjMxLjgyIDE3LjA5IDIzMS44MiAxNy44MFpNMjQ1LjI4IDE1LjQ4TDI0Mi42OSAxNS40OEwyNDIuNjkgMTMuNjBMMjUwLjIyIDEzLjYwTDI1MC4yMiAxNS40OEwyNDcuNjUgMTUuNDhMMjQ3LjY1IDIyTDI0NS4yOCAyMkwyNDUuMjggMTUuNDhaTTI2MS4zMyAyMkwyNTQuNTkgMjJMMjU0LjU5IDEzLjYwTDI2MS4xOCAxMy42MEwyNjEuMTggMTUuNDRMMjU2Ljk0IDE1LjQ0TDI1Ni45NCAxNi44NUwyNjAuNjggMTYuODVMMjYwLjY4IDE4LjYzTDI1Ni45NCAxOC42M0wyNTYuOTQgMjAuMTdMMjYxLjMzIDIwLjE3TDI2MS4zMyAyMlpNMjcwLjY4IDIyTDI2Ni4xNCAyMkwyNjYuMTQgMTMuNjBMMjcwLjQ0IDEzLjYwUTI3Mi4wNCAxMy42MCAyNzIuODggMTQuMTlRMjczLjcyIDE0Ljc5IDI3My43MiAxNS43OUwyNzMuNzIgMTUuNzlRMjczLjcyIDE2LjM5IDI3My40MyAxNi44N1EyNzMuMTMgMTcuMzQgMjcyLjU5IDE3LjYyTDI3Mi41OSAxNy42MlEyNzMuMzEgMTcuODcgMjczLjcyIDE4LjQxUTI3NC4xMyAxOC45NCAyNzQuMTMgMTkuNzBMMjc0LjEzIDE5LjcwUTI3NC4xMyAyMC44MCAyNzMuMjQgMjEuNDBRMjcyLjM1IDIyIDI3MC42OCAyMkwyNzAuNjggMjJaTTI2OC40OSAxOC41OEwyNjguNDkgMjAuMjhMMjcwLjQ4IDIwLjI4UTI3MS43MyAyMC4yOCAyNzEuNzMgMTkuNDNMMjcxLjczIDE5LjQzUTI3MS43MyAxOC41OCAyNzAuNDggMTguNThMMjcwLjQ4IDE4LjU4TDI2OC40OSAxOC41OFpNMjY4LjQ5IDE1LjMxTDI2OC40OSAxNi45NEwyNzAuMTIgMTYuOTRRMjcxLjMyIDE2Ljk0IDI3MS4zMiAxNi4xMkwyNzEuMzIgMTYuMTJRMjcxLjMyIDE1LjMxIDI3MC4xMiAxNS4zMUwyNzAuMTIgMTUuMzFMMjY4LjQ5IDE1LjMxWk0yNzguNDIgMTcuODBMMjc4LjQyIDE3LjgwUTI3OC40MiAxNi41NSAyNzkuMDIgMTUuNTVRMjc5LjYyIDE0LjU2IDI4MC42OSAxNC4wMFEyODEuNzUgMTMuNDMgMjgzLjA4IDEzLjQzTDI4My4wOCAxMy40M1EyODQuNDEgMTMuNDMgMjg1LjQ4IDE0LjAwUTI4Ni41NCAxNC41NiAyODcuMTUgMTUuNTVRMjg3Ljc1IDE2LjU1IDI4Ny43NSAxNy44MEwyODcuNzUgMTcuODBRMjg3Ljc1IDE5LjA1IDI4Ny4xNSAyMC4wNFEyODYuNTQgMjEuMDQgMjg1LjQ4IDIxLjYwUTI4NC40MiAyMi4xNyAyODMuMDggMjIuMTdMMjgzLjA4IDIyLjE3UTI4MS43NSAyMi4xNyAyODAuNjkgMjEuNjBRMjc5LjYyIDIxLjA0IDI3OS4wMiAyMC4wNFEyNzguNDIgMTkuMDUgMjc4LjQyIDE3LjgwWk0yODAuODEgMTcuODBMMjgwLjgxIDE3LjgwUTI4MC44MSAxOC41MSAyODEuMTIgMTkuMDVRMjgxLjQyIDE5LjYwIDI4MS45MyAxOS45MFEyODIuNDUgMjAuMjAgMjgzLjA4IDIwLjIwTDI4My4wOCAyMC4yMFEyODMuNzIgMjAuMjAgMjg0LjI0IDE5LjkwUTI4NC43NSAxOS42MCAyODUuMDUgMTkuMDVRMjg1LjM1IDE4LjUxIDI4NS4zNSAxNy44MEwyODUuMzUgMTcuODBRMjg1LjM1IDE3LjA5IDI4NS4wNSAxNi41NFEyODQuNzUgMTYgMjg0LjI0IDE1LjcwUTI4My43MiAxNS40MCAyODMuMDggMTUuNDBMMjgzLjA4IDE1LjQwUTI4Mi40NCAxNS40MCAyODEuOTMgMTUuNzBRMjgxLjQyIDE2IDI4MS4xMiAxNi41NFEyODAuODEgMTcuMDkgMjgwLjgxIDE3LjgwWk0yOTIuMDUgMTcuODBMMjkyLjA1IDE3LjgwUTI5Mi4wNSAxNi41NSAyOTIuNjYgMTUuNTVRMjkzLjI2IDE0LjU2IDI5NC4zMiAxNC4wMFEyOTUuMzkgMTMuNDMgMjk2LjcyIDEzLjQzTDI5Ni43MiAxMy40M1EyOTguMDUgMTMuNDMgMjk5LjExIDE0LjAwUTMwMC4xNyAxNC41NiAzMDAuNzggMTUuNTVRMzAxLjM5IDE2LjU1IDMwMS4zOSAxNy44MEwzMDEuMzkgMTcuODBRMzAxLjM5IDE5LjA1IDMwMC43OCAyMC4wNFEzMDAuMTcgMjEuMDQgMjk5LjExIDIxLjYwUTI5OC4wNSAyMi4xNyAyOTYuNzIgMjIuMTdMMjk2LjcyIDIyLjE3UTI5NS4zOSAyMi4xNyAyOTQuMzIgMjEuNjBRMjkzLjI2IDIxLjA0IDI5Mi42NiAyMC4wNFEyOTIuMDUgMTkuMDUgMjkyLjA1IDE3LjgwWk0yOTQuNDUgMTcuODBMMjk0LjQ1IDE3LjgwUTI5NC40NSAxOC41MSAyOTQuNzUgMTkuMDVRMjk1LjA1IDE5LjYwIDI5NS41NyAxOS45MFEyOTYuMDggMjAuMjAgMjk2LjcyIDIwLjIwTDI5Ni43MiAyMC4yMFEyOTcuMzYgMjAuMjAgMjk3Ljg3IDE5LjkwUTI5OC4zOSAxOS42MCAyOTguNjkgMTkuMDVRMjk4Ljk4IDE4LjUxIDI5OC45OCAxNy44MEwyOTguOTggMTcuODBRMjk4Ljk4IDE3LjA5IDI5OC42OSAxNi41NFEyOTguMzkgMTYgMjk3Ljg3IDE1LjcwUTI5Ny4zNiAxNS40MCAyOTYuNzIgMTUuNDBMMjk2LjcyIDE1LjQwUTI5Ni4wOCAxNS40MCAyOTUuNTcgMTUuNzBRMjk1LjA1IDE2IDI5NC43NSAxNi41NFEyOTQuNDUgMTcuMDkgMjk0LjQ1IDE3LjgwWk0zMDguNDcgMjJMMzA2LjEyIDIyTDMwNi4xMiAxMy42MEwzMDguNDcgMTMuNjBMMzA4LjQ3IDE3LjA5TDMxMS43MiAxMy42MEwzMTQuMzQgMTMuNjBMMzEwLjkxIDE3LjMyTDMxNC41MiAyMkwzMTEuNzYgMjJMMzA5LjM2IDE4Ljk1TDMwOC40NyAxOS45MEwzMDguNDcgMjJaIiBmaWxsPSIjRkZGRkZGIiB4PSIxMjYuMzEiLz48L3N2Zz4=)](https://forthebadge.com)
