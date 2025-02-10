# Implement Customer Information Input

- Prompt the user to enter the following customer details: first name, last name, email, phone number, address, and customer ID. Ensure all fields are mandatory except for the phone number.
- Validate the email format and ensure uniqueness within the system.

## Code Implementation

```python
# Example Python Code for Illustration
class CustomerRegistration:
    def __init__(self):
        self.existing_emails = set()

    def register_customer(self, first_name, last_name, email, phone, address, customer_id):
        if not first_name or not last_name or not email or not address or not customer_id:
            raise ValueError("All fields except phone number are mandatory.")
        if not self.is_valid_email(email) or email in self.existing_emails:
            raise ValueError("Invalid or duplicate email.")
        # Proceed with customer registration...
        self.existing_emails.add(email)

    def is_valid_email(self, email):
        import re
        return re.match(r"[^@]+@[^@]+\.[^@]+", email)
```

Make sure the actual system implementation aligns with the broader system architecture and coding practices.

