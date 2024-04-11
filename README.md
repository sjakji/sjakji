import random

# Define a class for the Uber driver
class UberDriver:
    def __init__(self, name, phone_number, email):
        self.name = name
        self.phone_number = phone_number
        self.email = email

    def pick_up_rider(self, location):
        print(f"{self.name} is on their way to {location} to pick up the rider.")

    def drop_off_rider(self, destination):
        print(f"{self.name} has arrived at {destination} and is dropping off the rider.")

# Define a function to request an Uber ride
def request_uber(location, destination, rider_contact_info):
    # Simulate the Uber driver being assigned to the ride
    driver_name = random.choice(["John", "Jane", "Mike", "Sarah"])
    driver_phone_number = "555-555-5555"
    driver_email = "driver@example.com"
    driver = UberDriver(driver_name, driver_phone_number, driver_email)

    # Print the rider's contact information
    print(f"Rider contact information: {rider_contact_info}")

    # Simulate the Uber driver picking up the rider
    driver.pick_up_rider(location)

    # Simulate the Uber driver dropping off the rider
    driver.drop_off_rider(destination)

# Example usage
location = "123 Main St"
destination = "456 Elm St"
rider_contact_info = "Rider phone number: 111-111-1111, Rider email: rider@example.com"
request_uber(location, destination, rider_contact_info)
