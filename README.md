import itertools
import string

def crack_password(password, max_length):
    # Generate all possible combinations of characters
    for length in range(1, max_length + 1):
        for attempt in itertools.product(string.ascii_letters + string.digits, repeat=length):
            attempt = ''.join(attempt)
            if attempt == password:
                print(f"Password cracked: {attempt}")
                return
