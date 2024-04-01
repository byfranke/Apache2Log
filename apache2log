#!/bin/bash

# Define the path to the Apache access log file
ACCESS_LOG="/var/log/apache2/access.log"

function show_last_entries() {
    echo "Displaying the last 100 entries of the Apache access log:"
    sudo tail -n 100 "$ACCESS_LOG"
}

function show_interactive_log() {
    echo "Opening the Apache access log interactively:"
    sudo less "$ACCESS_LOG"
}

function follow_log() {
    echo "Following the Apache access log in real time:"
    sudo tail -f "$ACCESS_LOG"
}

function show_unique_ips() {
    echo "Displaying the last 100 unique IP addresses that accessed the server:"
    awk '{print $1}' "$ACCESS_LOG" | sort | uniq | tail -n 100
}

function main_menu() {


    echo "     \                         |           ___ \   |                   "
    echo "    _ \    __ \    _` |   __|  __ \    _ \    ) |  |       _ \    _` | "
    echo "   ___ \   |   |  (   |  (     | | |   __/   __/   |      (   |  (   | "
    echo " _/    _\  .__/  \__,_| \___| _| |_| \___| _____| _____| \___/  \__, | "
    echo "          _|                                                    |___/  "
    echo "                  https://github.com/byfranke                          "
    echo "                                                                       "
    echo "Choose an option to proceed:"
    echo "1) Show the last 100 entries of the Apache access log"
    echo "2) Open the Apache access log interactively"
    echo "3) Follow the Apache access log in real time"
    echo "4) Show the last 100 unique IP addresses"
    echo "5) Exit"

    read -p "Enter your choice (1/2/3/4/5): " choice

    case "$choice" in
        1)
            show_last_entries
            ;;
        2)
            show_interactive_log
            ;;
        3)
            follow_log
            ;;
        4)
            show_unique_ips
            ;;
        5)
            echo "Exiting script."
            exit 0
            ;;
        *)
            echo "Invalid option selected. Please try again."
            main_menu
            ;;
    esac
}

main_menu
