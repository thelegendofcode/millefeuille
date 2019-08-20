# Development Roadmap

Document what the requirements of the app are, features being planned, and so on.

- [Requirements](#Requirements)
    - [User Persona #1](#user-persona-1)
    - [Developer](#developer)
- [v0.1.0 Minimally Usable Prototype](#v010-Minimally-Usable-Prototype)
    - [List of features](#List-of-features)
    - [List of user stories](#List-of-user-stories)
- [Features for some unknown future](#Features-for-some-unknown-future)

## Requirements

Requirements for who?

### [User Persona #1](user-persona.md)

- buys and holds stocks
- has multiple types of accounts (taxed, deferred, pension)
- holds stocks and cash balances in multiple currencies
- wants to see trading history
- wants to see growth history
- wants to see difference between principal and current values
- wants to know which stocks have had the best growth (%)
- wants to know how each account has fared
- wants to see predicted growth rates
- wants to see current asset allocation

### Developer

- user authentication
- various data structures
    - how to store market data
    - how to separate accounts/ledgers
    - how to store stock data
- input methods (add/edit/delete)
    - how to add a stock
    - how to add a new trade
    - how to import trading history (CSV)
    - how to import current portfolio balances
    - how to handle forex

## v0.1.0 Minimally Usable Prototype

Not to be mistaken with the Minimally Viable Prototype. What is *usable* isn't necessarily *viable*. Based on the above requirements, I've created a list of features that should approximate a usable app.

### List of features
1. User authentication
    1. log in with Google
1. Portfolio manager
    1. show list of stocks
    1. show details of individual stock
    1. add/edit/delete* a stock
    1. show list of user's accounts
    1. add/edit/delete* accounts
    1. add trading history
    1. add forex history
    1. market data of stocks held
    1. current market value of stock in account
        1. price bought average
        1. current price
        1. total value
        1. gains/losses (relative/absolute)
        1. total value of accounts in primary currency

NOTE: add/edit/delete are essentially 3 separate features.

Just having a list of features isn't very helpful. By itself, a feature lacks context. Converting them into user stories lets us group features together to create a better understanding of how they flow and connect with each other. A side benefit is that we can avoid listing 'obvious' features like show list of *X*.

### List of user stories
1. User wants to sign in to Millefeuille using their gmail account
1. User wants to create multiple portfolios
    - iDeco
    - NISA
    - standard account
1. User wants to add currently held stocks to portfolio
    - necessary fields: ticker symbol, full name
    - nice to haves: quantity, current value, link, buy price, currency
1. User wants to add trading history to portfolio
    - current balance and trade history don't have to match
    - will have to differentiate between add new and add history
    - group discrepency into a buffer
    - input form
    - import CSV
1. User wants a dashboard displaying portfolios' values
    - show principal vs current value
    - gains/losses in % and absolute numbers
    - up and down arrows
    - red for gains, blue for losses
1. User wants to see asset allocation percentages
    - create groups to stock certain stocks
    - show % break down of stocks in a group
    - compare groups (???)

It's not comprehensive but it's a good enough start. Some details are left out on purpose while others are overly detailed. They're more or less listed in order of priority so we can work our way down the list.

## Features for some unknown future
1. Expenses tracker
    - simply input and list all expenses
    - sorting/organisation/books can come later
1. Budget planner
