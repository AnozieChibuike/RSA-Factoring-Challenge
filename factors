#!/usr/bin/python3

import sys

def factorize_number(n):
    divisor = 2

    while n > 1:
        if n % divisor == 0:
            return divisor, n // divisor
        divisor += 1

def main():
    if len(sys.argv) != 2:
        print("Usage: factors.py <file>")
        sys.exit(1)

    input_file = sys.argv[1]

    try:
        with open(input_file, 'r') as file:
            for line in file:
                number = int(line.strip())
                p, q = factorize_number(number)
                print(f"{number}={p}*{q}")

    except FileNotFoundError:
        print(f"File not found: {input_file}")
        sys.exit(1)
    except ValueError:
        print(f"Invalid number in the file: {input_file}")
        sys.exit(1)

if __name__ == "__main__":
    main()