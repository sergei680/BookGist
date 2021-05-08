# 📚 BookGist: Unlock the Essence of Every Book  

**BookGist** is an AI-powered tool that delivers concise and insightful summaries of books, chapter by chapter. Whether you're a student, professional, or an avid reader, **BookGist** helps you grasp the core ideas quickly, saving you time and enhancing your understanding without compromising the depth of the original content.  

## 🔍 Why Use BookGist?  

- **Save Time**: Get to the heart of a book without reading it cover to cover.  
- **Enhance Understanding**: Reinforce knowledge by summarizing key points.  
- **Focus on What's Important**: Skip unnecessary details and focus on essential insights.  
- **Flexible Reading**: Ideal for reviewing material or catching up on readings.  

## 🌟 Features  

- **Chapter-wise Summarization**: Generates summaries for each chapter, allowing you to focus on specific sections.  
- **Whole Book Summarization**: For books without chapters, **BookGist** condenses the entire text into a comprehensive summary.  
- **Advanced NLP Techniques**: Utilizes cutting-edge Natural Language Processing models to extract meaningful information.  
- **User-Friendly Interface**: Accessible to users of all technical backgrounds with a clean and intuitive design.  
- **Email Delivery Option**: Receive your summaries directly in your inbox for convenience.  

## 🛠️ How It Works  

**BookGist** leverages the `T5-small` pretrained model from HuggingFace Transformers to generate accurate and coherent summaries. Here's a breakdown of the process:  

1. **Text Segmentation**: The input book (in PDF format) is divided into chunks based on chapters. If the book lacks chapters, it's treated as a single chunk.  
2. **Tokenization**: Each chunk is tokenized using the `T5Tokenizer` to prepare it for the model.  
3. **Summary Generation**: The tokenized text is fed into the `T5ForConditionalGeneration` model, which generates summarized content.  
4. **Decoding**: The output tokens are decoded back into human-readable text using the `decode()` function of `T5Tokenizer`.  
5. **Compilation**: All summarized chunks are compiled into a final summary document.  

## 🚀 Getting Started  

### Prerequisites  

- **Python 3.x**  
- **Pip** (Python package installer)  

### Installation  

1. **Clone the Repository**  
  
   ```bash  
   git clone https://github.com/loganreedd/BookGist.git  
   ```  

2. **Navigate to the Project Directory**  
  
   ```bash  
   cd BookGist  
   ```  

3. **Install Dependencies**  
  
   Install all required Python packages using:  
  
   ```bash  
   pip install -r requirements.txt  
   ```  

### Usage  

#### Command-Line Interface (CLI)  

To run **BookGist** via the command line:  

```bash  
python3 summarizer_cli.py --path <path-to-your-PDF-file>  
```  

- Replace `<path-to-your-PDF-file>` with the actual file path of the book you want to summarize.  

#### Web Application Using Flask  

**BookGist** also offers a web interface for a more interactive experience.  

1. **Configure Email Settings**  
  
   - Open `mail.py` and update the following variables with your email credentials:  
  
     ```python  
     sender_address = 'your_email@example.com'  
     sender_pass = 'your_email_password'  
     ```  
  
   - This allows the application to send the summary to your email address.  

2. **Run the Flask App**  
  
   ```bash  
   python3 app.py  
   ```  

3. **Access the Web Interface**  
  
   - Open your web browser and navigate to `http://localhost:5000`.  

4. **Upload and Summarize**  
  
   - Use the interface to upload a PDF file and enter your email address to receive the summary.  

### Example  

Here's how you might run the CLI:  

```bash  
python3 summarizer_cli.py --path 'books/Interesting_Book.pdf'  
```  

## 📫 Receiving Summaries via Email  

- Ensure you've configured your email settings in `mail.py`.  
- The summary will be sent to the email address you provide when using the web interface.  

## 🤝 Contributing  

We welcome contributions from the community! To contribute to **BookGist**, please follow these steps:  

1. **Fork the Repository**  
  
   Click on the 'Fork' button at the top right corner of this page to create a copy of this repository on your GitHub account.  

2. **Clone Your Fork**  
  
   ```bash  
   git clone https://github.com/loganreedd/BookGist.git  
   ```  

3. **Create a New Branch**  
  
   ```bash  
   git checkout -b feature/YourFeature  
   ```  

4. **Commit Your Changes**  
  
   ```bash  
   git commit -am 'Add a new feature'  
   ```  

5. **Push to Your Branch**  
  
   ```bash  
   git push origin feature/YourFeature  
   ```  

6. **Submit a Pull Request**  
  
   Go to the original repository on GitHub and create a pull request from your forked repository.  

## 📄 License  

**BookGist** is licensed under the [MIT License](LICENSE).  

## 📧 Contact  

For any questions or suggestions, feel free to open an issue or contact the maintainer:  

- **Your Name**  
- **Email**: <your_email@example.com>  
- **GitHub**: [loganreedd](https://github.com/loganreedd)  

---  

*Crafted with ❤️ by [Your Name](https://github.com/loganreedd)*  

---  

## 🔗 Links  

- [Project Repository](https://github.com/loganreedd/BookGist)  
- [Issue Tracker](https://github.com/loganreedd/BookGist/issues)  

## ❤️ Acknowledgments  

- Thanks to the developers of [HuggingFace Transformers](https://github.com/huggingface/transformers) for their powerful NLP models.  
- Inspired by the need to make reading more accessible and efficient.  

---  

**BookGist** — *Unlock the essence of every book.*
