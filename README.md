# challenge_2

# Loan Application

This project uses a command line interface where applicants input financial information and recieve a list of qualifying loans as a .csv file. 

---

## Technologies

The project is written in python 3.9 and uses the sys, csv, fire, questionary and pathlib libraries.

---

## Installation Guide

Users may run the program in an IDE of their choice. 

---

## Usage

Running the program returns a CLI where users input financial data. The application terminates if users are unwilling to save the data or do not qualify for any loans. CSV file is saved in user-provided location under the name "qualifying_loans.csv"

     # ask applicant if they would like to save loan
    loan_save_question = questionary.confirm("Would you like to save your qualifying loans?").ask()

    # if answer is no, exit program
    if loan_save_question == False:  
        sys.exit("OK, thanks for your time")

    # if applicant doesn't qualify, terminate program
    elif qualifying_loans==[]:
        sys.exit("Sorry you don't qualify for any loans")
        
    # ask applicant for file location and add "qualifying_loans.csv" to path
    loan_location = questionary.text("Where would you like the file saved?").ask()+"qualifying_loans.csv"
    loan_save_path= Path(loan_location)    
---

## Contributors

The project was completed by jbena4 under the direction of instructors with the Columbia Engineering certificate program.

---

## License

This project is free to distribute and licensed under MIT.
