# Reproduce the bug from https://github.com/felangel/mason/issues/496

1. ```mason get```
2. ```mason make normal_brick```
*If your user_name is longer than 5 characters – make short_brick instead*

Everything should be fine now. You can check your longest path at C:\Users\user_name\AppData\Local\Mason\Cache\git\mason_windows_bricks_bug_aHR0cHM6Ly9naXRodWIuY29tL0xlZ2VuZG9yaWsvbWFzb25fd2luZG93c19icmlja3NfYnVnLmdpdA==_40f625cad39032c0018181afd3034d91aaed9d33\normal_brick\...
It should be less then 260 symbols.

3. In mason.yaml uncomment bugged_brick
4. ```mason get```
5. See FileSystemException

