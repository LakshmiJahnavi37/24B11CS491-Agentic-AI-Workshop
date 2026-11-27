# Sports ShopMate AI

**A Bilingual Sports Equipment Shopping Assistant using Groq, LangChain Agents, and Google Sheets**

## Project Overview

Sports ShopMate AI is an AI-powered shopping assistant designed for a sports equipment store. It helps customers explore sports products, check prices and availability, receive budget-based recommendations, and place orders through a conversational chatbot.

The chatbot supports both **English and Telugu**, making shopping easier and more accessible.

## Technologies Used

- Python
- Google Colab
- Groq API – `openai/gpt-oss-120b`
- LangChain Agents
- Google Sheets
- Pydantic

## Key Features

1. **Bilingual Conversations:** Communicates with customers in English and Telugu.
2. **Product Information:** Provides product details, categories, sizes, colours, prices, and stock availability.
3. **Price Calculation:** Calculates the total price based on product quantity.
4. **Budget-Based Recommendations:** Suggests sports equipment according to the customer's budget.
5. **Order Management:** Collects customer and product details and saves confirmed orders.
6. **Google Sheets Integration:** Automatically records confirmed orders in Google Sheets.
7. **Conversation Memory:** Maintains context during the current conversation.

## Product Categories

The chatbot includes sample products from:

- Cricket
- Football
- Badminton
- Tennis
- Basketball
- Volleyball
- Table Tennis
- Fitness
- Gym Equipment
- Athletics

## AI Agent Tools

| Tool | Function |
|---|---|
| `get_price` | Checks product prices and calculates totals |
| `check_product` | Checks product details and availability |
| `recommend_products` | Recommends products based on budget |
| `log_order` | Saves confirmed customer orders to Google Sheets |

## How It Works

1. The customer interacts with the chatbot in English or Telugu.
2. The AI agent understands the customer's request.
3. It selects the appropriate tool to retrieve product information.
4. Customers can check prices, availability, and recommendations.
5. For purchases, the chatbot collects and validates order details.
6. After customer confirmation, the order is saved to Google Sheets.

## Google Sheets Integration

Confirmed orders are stored with the following details:

- Customer Name
- Product
- Category
- Quantity
- Size / Specification
- Colour
- Order Date
- Total Amount (Rs)

## How to Run

1. Open the project in Google Colab.
2. Install the required Python libraries.
3. Add your Groq API key to Colab Secrets using the name `AgenticAI`.
4. Run the Google Sheets authentication cell.
5. Execute the remaining notebook cells in order.
6. Start interacting with Sports ShopMate AI.

## Note

The product catalogue, prices, and stock quantities are sample demonstration data. They should be updated with actual store inventory before real-world use.

## Future Enhancements

- Real-time inventory updates.
- Payment gateway integration.
- Order tracking.
- Product images and catalog browsing.
- Customer purchase history.
- Integration with an online sports store.

---

**Sports ShopMate AI – Your Smart Assistant for Sports Shopping!**
