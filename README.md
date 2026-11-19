# Cos-201
import math


def get_primes(limit):
    primes = []
    # Prime numbers start at 2
    for num in range(2, limit + 1):
        is_prime = True
        # Check for factors up to the square root of num
        for i in range(2, int(math.sqrt(num)) + 1):
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            primes.append(num)
    return primes


# Find and print primes up to 500
primes_up_to_500 = get_primes(500)
print(f"Found {len(primes_up_to_500)} prime numbers:")
print(primes_up_to_500)
