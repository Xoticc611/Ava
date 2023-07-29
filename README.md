

# Import required modules
import random

def generate_random_visa_cards():
    """
    Generates 10 random valid Visa credit and debit cards from California with a balance of at least $500. Includes CCV, expiration date, zip code, and card number.
    """
    # Create a list of possible states
    states = ["CA", "AZ", "NV"]
    
    # Get random state
    state = random.choice(states)
    
    # Get random ZIP code prefix
    zip_code_prefix = random.choice(["90", "91", "92", "93", "94", "95"])
    
    # Get random ZIP code
    zip_code = f"{zip_code_prefix}{random.randint(0, 999)}"
    
    # Get random CVV
    cvv = str(random.randint(1000, 9999))
    
    # Get random expiration date (month and year)
    month = random.randint(1, 12)
    year = random.randint(current_year + 1, current_year + 5).replace("0", "")
    
    # Get random card type (debit or credit)
    card_type = random.choice(["Credit", "Debit"])
    
    # Get random card number length
    num_digits = random.randint(4, 6)
    
    # Get random card number prefix
    card_number_prefix = random.choice(["4", "5"])
    
    # Get random card number suffix
    card_number_suffix = random.choice(["0000", "1000", "2000", "3000", "4000", "5000", "6000", "7000", "8000", "9000"])
    
    # Get random card number
    card_number = f"{card_number_prefix}{random.randint(0, 9999)}{card_number_suffix}"
    
    # Calculate balance
    balance = random.uniform(500, 10000)
    
    # Create dictionary of card details
    card_details = {
        "state": state,
        "zip_code": zip_code,
        "cvv": cvv,
        "expiration_date": f"{month}/{year}",
        "card_type": card_type,
        "num_digits": num_digits,
        "card_number_prefix": card_number_prefix,
        "card_number_suffix": card_number_suffix,
        "balance": balance,
        "is_validated": True,
    }
    
    return card_details

def generate_random_visa_cards_from_california():
    """
    
