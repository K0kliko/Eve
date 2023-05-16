@echo off
color f
title Eve
cls

:choice
set /p choice=Do you really want to put your PC to sleep (y/n)

    if /i "%choix%"=="y" (goto :yes)
    if /i "%choix%"=="n" (goto :no)
    goto :ERROR

:yes

    cls
    echo Your PC will go to sleep.
    pause
    shutdown /h
    exit

:no
    cls
    echo Your PC will not sleep.
    pause
    exit

:ERROR
    echo ERROR : Please choose between y (yes) or n (no).
    pause
    cls
    goto :choice
