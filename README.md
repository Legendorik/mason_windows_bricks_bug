# Reproduce the bug from https://github.com/felangel/mason/issues/496

1. Try ```mason get```
2. See FileSystemException. It will point on bugged_brick.
3. Manually delete the bugged_brick folder from C:\Users\user_name\AppData\Local\Mason\Cache\git\mason_windows_bricks_bug_aHR0cHM6Ly9naXRodWIuY29tL0xlZ2VuZG9yaWsvbWFzb25fd2luZG93c19icmlja3NfYnVnLmdpdA==_40f625cad39032c0018181afd3034d91aaed9d33\

*If your user_name is longer than 5 characters – delete normal_brick too and comment it in mason.yaml*
4. Try ```mason get``` again

Everything should be fine now. You can check your longest path at C:\Users\user_name\AppData\Local\Mason\Cache\git\mason_windows_bricks_bug_aHR0cHM6Ly9naXRodWIuY29tL0xlZ2VuZG9yaWsvbWFzb25fd2luZG93c19icmlja3NfYnVnLmdpdA==_40f625cad39032c0018181afd3034d91aaed9d33\normal_brick\...
It should be less then 260 symbols.

Sometimes you can successfully execute ```mason get``` for some strange reason, but can't ```mason make bugged_brick``` instead.


