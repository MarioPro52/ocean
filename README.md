# oceanclass Ocean:
    def __init__(self, name, size):
        self.name = name
        self.size = size  # in square kilometers
        self.marine_life = []

    def add_marine_species(self, species):
        """Add a species to the ocean's marine life."""
        self.marine_life.append(species)
        print(f"{species} has been added to the {self.name}.")

    def remove_marine_species(self, species):
        """Remove a species from the ocean's marine life."""
        if species in self.marine_life:
            self.marine_life.remove(species)
            print(f"{species} has been removed from the {self.name}.")
        else:
            print(f"{species} is not found in the {self.name}.")

    def display_info(self):
        """Display information about the ocean."""
        print(f"Ocean Name: {self.name}")
        print(f"Size: {self.size} square kilometers")
        print("Marine Life: " + ", ".join(self.marine_life) if self.marine_life else "No marine life added yet.")

# Example usage
pacific_ocean = Ocean("Pacific Ocean", 168723000)
pacific_ocean.display_info()  # Display initial info
pacific_ocean.add_marine_species("Dolphin")  # Add a species
pacific_ocean.add_marine_species("Whale")    # Add another species
pacific_ocean.display_info()  # Display updated info
pacific_ocean.remove_marine_species("Dolphin")  # Remove a species
pacific_ocean.display_info()  # Display updated info
