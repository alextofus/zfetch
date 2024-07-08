#!/bin/bash

# Get system information
OS=$(grep '^PRETTY_NAME=' /etc/os-release | cut -d= -f2 | tr -d '"')
KERNEL=$(uname -r | cut -d'-' -f1)
WM=$(echo $XDG_CURRENT_DESKTOP)
TYPE="Computer"

# Adjust the lengths of the fields
OS_FIELD="OS: $OS"
KERNEL_FIELD="Kernel: $KERNEL"
WM_FIELD="WM: $WM"
TYPE_FIELD="Type: $TYPE"

# Determine the max length for proper alignment
MAX_LENGTH=$(echo -e "$OS_FIELD\n$KERNEL_FIELD\n$WM_FIELD\n$TYPE_FIELD" | wc -L)

# Print the information
echo "╭────────INFO────────╮"
printf "│ %-*s     │\n" $((MAX_LENGTH)) "$OS_FIELD"
printf "│ %-*s     │\n" $((MAX_LENGTH)) "$KERNEL_FIELD"
printf "│ %-*s     │\n" $((MAX_LENGTH)) "$WM_FIELD"
printf "│ %-*s     │\n" $((MAX_LENGTH)) "$TYPE_FIELD"
echo "╰────────────────────╯"
