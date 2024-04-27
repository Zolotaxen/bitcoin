# bitcoin
from bitcoinlib.wallets import Wallet

# Create a new wallet
wallet = Wallet.create('MyWallet')

# Generate a new address for receiving payments
new_address = wallet.get_new_address()

print("New Address:", new_address)

# Check wallet balance
balance = wallet.balance()
print("Wallet Balance:", balance)

# Send bitcoins
recipient_address = '1ABCXYZ123456...'
amount_to_send = 0.001  # Amount in BTC
txid = wallet.send_to(recipient_address, amount_to_send)

print("Transaction ID:", txid)
