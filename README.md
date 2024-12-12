# PyTorrent

PyTorrent is a simple and feature-rich BitTorrent client written in Python. It allows users to download, upload, and manage torrents with support for DHT, PEX, encryption, speed control, RSS feeds, and a built-in chat feature. This project is perfect for learning about torrenting, networking, and working with the BitTorrent protocol.
Features

    Torrent downloading: Supports .torrent files and magnet links.
    Seeding: Automatically seeds downloaded files.
    DHT (Distributed Hash Table): Allows decentralized peer discovery.
    PEX (Peer Exchange): Improves peer discovery by sharing peer information between clients.
    Encryption: Supports encryption for secure communication between peers.
    Speed Control: Allows users to set download and upload speed limits.
    RSS Feeds: Automatically fetch and download new torrents from an RSS feed.
    Chat Server: A simple built-in chat feature for communication between clients (optional).

Installation
Requirements

    Python 3.x
    libtorrent library
    feedparser library

Installing Dependencies

To get started, you need to install the required libraries:

pip install python-libtorrent feedparser

Clone the Repository

Clone the PyTorrent repository to your local machine:

git clone https://github.com/nazarhktwitch/PyTorrent
cd PyTorrent

Usage
Running the Torrent Client

To start the torrent client, you can either provide a magnet link or a torrent file to begin downloading. For example:

# Initialize the client with a .torrent file
client = TorrentClient(torrent_file='path_to_torrent_file.torrent', download_dir='./downloads/')

# Initialize the client with a magnet link
client = TorrentClient(magnet_link='magnet:?xt=urn:btih:...', download_dir='./downloads/')

After initializing the client, you can control the speed and start the download.
Set Speed Limits (optional)

You can limit download and upload speeds by using the set_speed_limits() function:

client.set_speed_limits(download_limit=100000, upload_limit=50000)

Start Downloading

Once initialized and configured, start the download process:

client.start_download()

Fetch Torrents from RSS Feeds (optional)

You can automatically fetch torrents from an RSS feed:

fetch_rss_feed('https://your-rss-feed-url.com')

Start the Chat Server (optional)

The chat feature allows communication between clients. To start the chat server:

chat_server()

Chat Server

The chat server enables real-time communication between clients. The server listens on port 9999 by default. Once connected, users can send messages to each other. You can also extend the server to support more features like multiple rooms or private chats.
Configuration

    DHT: By default, DHT is enabled, allowing for decentralized peer discovery.
    PEX: Peer Exchange is enabled to enhance peer discovery and improve download speeds.
    Encryption: Traffic encryption is enabled to ensure privacy during torrenting.

You can disable these features if needed by modifying the respective functions in the TorrentClient class.
Example: Complete Torrent Download and Chat Setup

import time
import threading
from pytorrent import TorrentClient, fetch_rss_feed, chat_server

# Initialize TorrentClient with a torrent file
client = TorrentClient(torrent_file='path_to_torrent_file.torrent', download_dir='./downloads/')

# Set speed limits
client.set_speed_limits(download_limit=100000, upload_limit=50000)

# Start downloading
client.start_download()

# Fetch new torrents from RSS feed (optional)
fetch_rss_feed('https://your-rss-feed-url.com')

# Start the chat server (optional)
chat_server()

Contributing

If you'd like to contribute to PyTorrent, feel free to fork the repository and create a pull request. All contributions are welcome, whether it's bug fixes, new features, or improvements to the documentation.

To contribute:

    Fork the repository.
    Create a new branch.
    Make your changes.
    Submit a pull request.

License

PyTorrent is released under the MIT License. See the LICENSE file for more details.
Contact

For any questions or issues, feel free to open an issue on the GitHub repository or reach out to us at:

Email: nazarburlan3@outlook.com

Enjoy torrenting with PyTorrent!
