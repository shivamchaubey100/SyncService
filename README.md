# SyncService Repository

This repository contains Python code for a simple synchronization service (`SyncService`) that handles communication with multiple devices (`Device`) to collect and store data. The primary purpose is to demonstrate a basic implementation of data synchronization between devices and a central server.

## Features

- Each `Device` generates new data points at random intervals.
- The `SyncService` handles incoming data records and probe requests from devices.
- The synchronization process involves sending data records from devices to the server and responding to probe requests with updates.

## Requirements

- Python 3.x

## How to Run

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/shivamchaubey100/DevCom_PS2.git
   ```

2. Navigate to the repository directory:

   ```bash
   cd DevCom_PS2
   ```

3. Run the `final_solution.py` file:

   ```bash
   python3 final_solution.py
   ```

   This will execute the `testSyncing` function, simulating the interaction between 10 devices and the `SyncService`. The synchronization process will be demonstrated, and assertions will be made to ensure the correctness of the implementation.

## Implementation Details

- `Device` class:
  - `obtainData()`: Generates a new data point with a type of 'record' containing device information and random data.
  - `probe()`: Generates a probe request to be sent to the `SyncService`.
  - `onMessage(data)`: Receives updates from the server and updates its records accordingly.

- `SyncService` class:
  - `onMessage(data)`: Handles messages received from devices. Stores data records and responds to probe requests with the appropriate updates.

## Testing

The `testSyncing` function is included in the code to demonstrate and validate the synchronization process. Assertions are made to ensure that the records received by the server match the records stored by each device.

**Note**: Uncomment the relevant code sections within `testSyncing` to print and verify additional information if needed.

Feel free to explore, modify, and integrate this synchronization service into your projects. If you encounter any issues or have suggestions for improvement, please open an issue or submit a pull request.

Happy coding!
