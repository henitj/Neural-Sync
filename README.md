## README.md

# Neural-Sync

**Neural-Sync** is a "from-scratch" implementation of a feedforward neural network. This project avoids heavy machine learning frameworks to focus on the fundamental mathematics of artificial intelligence, providing a clear view of how neurons process data and learn through error correction.

URL - https://neural-sync-theta.vercel.app/

## 🚀 Features
* **Custom Architecture:** Supports configurable layers and neuron counts.
* **Math-First Implementation:** Hand-coded matrix multiplication and activation functions (Sigmoid/ReLU).
* **Backpropagation:** Features a gradient descent optimizer to update weights based on calculated loss.
* **Real-time Visualization:** (If applicable) A dynamic canvas or DOM-based view of connections and their current weights/biases.
* **Data Normalization:** Built-in functions to scale input data for more efficient training.

## 🛠️ Technical Stack
* **JavaScript (ES6):** Core logic for the neural network and mathematical operations.
* **HTML5/CSS3:** UI for adjusting hyperparameters (learning rate, epochs) and viewing results.

## 🕹️ How to Use
1. **Clone the repository:**
   ```bash
   git clone https://github.com/HenitJain/Neural-Sync.git
   ```
2. **Launch:**
   * Open `index.html` in your browser.
3. **Execution:**
   * Input your training dataset (e.g., XOR logic gate values).
   * Set the number of iterations and learning rate.
   * Click **Train** and observe the loss decrease as the network "syncs" with the target output.

## 📂 Project Structure
* `network.js`: The central Brain class containing the network structure.
* `layer.js`: Defines individual layers and their transformation logic.
* `utils.js`: Helper functions for Sigmoid activation and derivative calculations.
* `README.md`: Documentation.

## ⚙️ Mathematical Foundation
The network processes data through **Forward Propagation**, where each layer's output is calculated as:
$$y = \text{activation}(\sum (weight \cdot input) + bias)$$

During **Backpropagation**, the error is sent backward through the network using the Chain Rule to calculate gradients, allowing the weights to be updated:
$$W_{new} = W_{old} - (\eta \cdot \frac{\partial Loss}{\partial W})$$
*(where $\eta$ is the learning rate)*
