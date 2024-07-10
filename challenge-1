function calculateGrade() {
        
        //////// grade based on marks////
        let grade;
        if (marks > 79) {
            grade = 'A';
        } else if (marks >= 60) {
            grade = 'B';
        } else if (marks >= 50) {
            grade = 'C';
        } else if (marks >= 40) {
            grade = 'D';
        } else {
            grade = 'E';
        }
        
            ////// Prompts the user for input///
             let marks = parseFloat(prompt("Enter student marks:"));
             
             ///// Validate input range//
             if (isNaN(marks) || marks < 0 || marks > 100) {
                 console.log("Invalid entry");
             }else{console.log(`The grade for ${marks} marks is: ${grade}`);}
}
