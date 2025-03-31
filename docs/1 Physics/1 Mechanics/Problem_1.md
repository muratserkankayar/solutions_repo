# Problem 1

import numpy as np
import matplotlib.pyplot as plt

def projectile_range(v0, g=9.81):
    angles = np.linspace(0, 90, 100)  # Angles between 0 and 90 degrees
    ranges = (v0**2 * np.sin(2 * np.radians(angles))) / g  # Range formula
    
    plt.figure(figsize=(8, 5))
    plt.plot(angles, ranges, label=f'Initial Velocity: {v0} m/s')
    plt.xlabel('Projection Angle (degrees)')
    plt.ylabel('Range (meters)')
    plt.title('Projectile Range vs. Angle of Projection')
    plt.legend()
    plt.grid()
    plt.show()

# Example usage
projectile_range(20)  # Plot range graph for an initial velocity of 20 m/s
