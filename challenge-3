function calculateNetSalary(basicSalary, benefits) {
    ////// Constants for tax rates/////
    const TAX_THRESHOLD = 5000;
    const TAX_RATE_LOW = 0.10;   
    const TAX_RATE_HIGH = 0.50;  

    ///// Constants for NHIF and NSSF deductions////
    const NHIF_RATE = 0.0003;  
    const NSSF_RATE_EMPLOYEE = 0.3; 

    ///// Calculate gross salary //////
    let grossSalary = basicSalary + benefits;

    /////Calculate NHIF deductions////
    let nhifDeductions = grossSalary * NHIF_RATE;

    //// Calculate NSSF deductions////
    let nssfDeductions = grossSalary * NSSF_RATE_EMPLOYEE;

    ///// Calculate taxable income////
    let taxableIncome = grossSalary - (nhifDeductions + nssfDeductions);

    ///// Calculate Payee////
    let payee;
    if (taxableIncome <= TAX_THRESHOLD) {
        payee = taxableIncome * TAX_RATE_LOW;
    } else {
        payee = TAX_THRESHOLD * TAX_RATE_LOW + (taxableIncome - TAX_THRESHOLD) * TAX_RATE_HIGH;
    }

    ////// Calculate net salary ///////
    let netSalary = grossSalary - (payee + nhifDeductions + nssfDeductions);
    return {
        grossSalary: grossSalary,
        nhifDeductions: nhifDeductions,
        nssfDeductions: nssfDeductions,
        payee: payee,
        netSalary: netSalary
    };
}
const basicSalary = parseFloat(prompt("Enter Basic Salary: "));
const benefits = parseFloat(prompt("Enter Benefits: "));

const salaryDetails = calculateNetSalary(basicSalary, benefits);
 
console.log("Salary Details:");
console.log(`Basic Salary: ${basicSalary}`);
console.log(`Benefits: ${benefits}`);
console.log(`Gross Salary: ${salaryDetails.grossSalary}`);
console.log(`NHIF Deductions: ${salaryDetails.nhifDeductions}`);
console.log(`NSSF Deductions: ${salaryDetails.nssfDeductions}`);
console.log(`Payee (Tax): ${salaryDetails.payee}`);
console.log(`Net Salary: ${salaryDetails.netSalary}`);
