import requests

# Replace with the actual blockchain explorer API endpoint
API_URL = "https://blockchain-explorer.example.com/api"

# Example block number and transaction signature
block_number = 315511280
transaction_signature = "2a4BFdxsFXtrotkpv3NmUNA..."

# Fetch block details
block_response = requests.get(f"{API_URL}/block/{block_number}")
block_data = block_response.json()

# Fetch transaction details
tx_response = requests.get(f"{API_URL}/transaction/{transaction_signature}")
tx_data = tx_response.json()

print("Block Data:", block_data)
print("Transaction Data:", tx_data)
