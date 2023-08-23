class FlightTable:
    def __init__(self):
        self.flights = []

    def add_flight(self, flight_id, source, destination, price):
        self.flights.append((flight_id, source, destination, price))

    def search_by_city(self, city):
        results = [flight for flight in self.flights if city in (flight[1], flight[2])]
        return results

    def search_from_city(self, source_city):
        results = [flight for flight in self.flights if flight[1] == source_city]
        return results

    def search_between_cities(self, source_city, destination_city):
        results = [flight for flight in self.flights if flight[1] == source_city and flight[2] == destination_city]
        return results

def main():
    flight_table = FlightTable()

    data = [
        ("AI161E90", "BLR", "BOM", 5600),
        ("BR161F91", "BOM", "BBI", 6750),
        ("AI161F99", "BBI", "BLR", 8210),
        ("VS171E20", "JLR", "BBI", 5500),
        ("AS171G30", "HYD", "JLR", 4400),
        ("AI131F49", "HYD", "BOM", 3499)
    ]

    for item in data:
        flight_table.add_flight(*item)

    while True:
        print("\nFlight Search Options:")
        print("1. Flights for a particular City")
        print("2. Flights From a city")
        print("3. Flights between two given cities")
        print("4. Exit")

        choice = input("Enter your choice (1/2/3/4): ")

        if choice == "1":
            city = input("Enter the city name: ")
            results = flight_table.search_by_city(city)
        elif choice == "2":
            source_city = input("Enter the source city name: ")
            results = flight_table.search_from_city(source_city)
        elif choice == "3":
            source_city = input("Enter the source city name: ")
            destination_city = input("Enter the destination city name: ")
            results = flight_table.search_between_cities(source_city, destination_city)
        elif choice == "4":
            break
        else:
            print("Invalid choice. Please enter a valid option.")
            continue

        if results:
            print("Flight ID\tSource\tDestination\tPrice")
            for item in results:
                print(item[0], "\t\t", item[1], "\t\t", item[2], "\t\t", item[3])
        else:
            print("No flights found for the given criteria.")

if __name__ == "__main__":
    main()
