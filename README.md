<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coding Assessment Rubic ©NabilTarrafKojok</title>
    <style>
    body {
        font-family: Arial, sans-serif;
    }

    .rating-app {
        max-width: 800px;
        margin: 0 auto;
        padding: 2px;
    }

    .section {
        border: 1px solid #ccc;
        padding: 10px;
        margin-bottom: 20px;
    }

    h2 {
        margin: 0;
    }

    .rating-table {
        width: 100%;
    }

    .rating-buttons {
        display: flex;
        flex-wrap: wrap;
    }

    .rating-buttons button {
        flex: 0 0 calc(25% - 10px);
        margin: 5px;
        padding: 5px 10px;
        background-color: #007BFF;
        color: white;
        border: none;
        cursor: pointer;
    }

    .rating-buttons button.active {
        background-color: #FF6B6B; /* Change to complement color */
    }

    .total-mark {
            font-size: 18px;
            font-weight: bold;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background-color: white;
            padding: 2px 0;
            z-index: 999;
        }
        
    button {
        background-color: #007BFF;
        color: white;
        border: none;
        padding: 10px 20px;
        cursor: pointer;
    }
    
    .table-container {
            margin-top: 5px; /* Adjust the top margin to make space for the fixed header */
        }

    /* Add page breaks as needed */
    .section:nth-child(3n) {
        page-break-before: always;
    }

    /* Move the "Documentation and Comments" section to a new page (page 3) */
    .section:nth-child(5) {
        page-break-before: always;
    }

    /* Reset page breaks for the first two sections */
    .section:nth-child(1), .section:nth-child(2) {
        page-break-before: auto;
    }

    /* @media print block remains unchanged */
    @media print {
        /* Preserve background and text colors for printing */
        .rating-app, .section, h2, .rating-buttons button {
            -webkit-print-color-adjust: exact;
            print-color-adjust: exact;
        }

        /* Specify background and text colors for printing as needed */
        body {
            background-color: white;
            color: black;
        }

        .section {
            background-color: lightblue !important;
        }

        .section:nth-child(2n) {
            background-color: lightgreen !important;
        }

        .section:nth-child(3n) {
            background-color: lightpink !important;
        }

        .section:nth-child(4n) {
            background-color: lightyellow !important;
        }

        .section:nth-child(5n) {
            background-color: lightcoral !important;
        }
    }
    
    /* Add styles for the table container */
        .table-container {
            display: flex;
            justify-content: center; /* Center the table horizontally */
        }

        /* Add styles for the table */
        .student-table {
            width: 800px; /* Set a fixed width to match the colored sections */
            border-collapse: collapse;
            margin-bottom: 1px;
        }

        .student-table th, .student-table td {
            width: calc(25% - 10px); /* Set width to match button width */
            border: 1px solid #fff; /* Format table lines to be white */
            padding: 5px 10px;
            text-align: left; /* Align headers left */
        }

        .student-input {
            width: 100%; /* Make input boxes full width of the cell */
            padding: 5px 10px;
            border: 1px solid #ccc;
            background-color: #f9f9f9;
            border-radius: 4px;
            box-sizing: border-box;
        }

        /* Style for the "Insert New Student" buttons */
        .insert-button {
            background-color: #007BFF;
            color: white;
            border: none;
            padding: 5px 10px;
            cursor: pointer;
        }

        /* Style for hidden input elements */
        .student-hidden {
            display: none;
        }
        
            
/* Add margin to sections 3 and 5 */
.section:nth-child(3), .section:nth-child(5) {
    margin-top: 60px; /* Adjust the margin as needed to create space */
}
       
</style>

</head>
<body>



		<div class="total-mark" id="fixedTotalMark">
        	<p>Total Mark: <span id="total-mark">0%</span></p>
    	</div>
       
       
       <!-- Add a placeholder div to create space for the fixed header -->
    <div style="height: 50px;"></div>
    
    
    <div class="table-container">
        <!-- Add student name input table at the top of the page -->
        <table class="student-table">
            <tr>
                <th id="studentHeader1">Student 1</th>
                <th>
                    <button class="insert-button" data-index="2">Insert New Student</button>
                </th>
                <th>
                    <button class="insert-button" data-index="3">Insert New Student</button>
                </th>
                <th>
                    <button class="insert-button" data-index="4">Insert New Student</button>
                </th>
            </tr>
            <tr>
                <td><input id="student1" class="student-input" type="text" placeholder="Enter name"></td>
                <td><input class="student-input student-hidden" type="text" placeholder="Enter name"></td>
                <td><input class="student-input student-hidden" type="text" placeholder="Enter name"></td>
                <td><input class="student-input student-hidden" type="text" placeholder="Enter name"></td>
            </tr>
        </table>
    </div>
       
    <div class="rating-app">
        <!-- Creativity and Originality -->
        <div class="section" style="background-color: lightblue;">
            <h2>Creativity and Originality</h2>
            <div class="rating-table">
                <div class="rating-buttons">
                    <!-- Rating buttons -->
                    <button onclick="recordScore(this, 'Creativity and Originality', 1, 1, 4)">Demonstrates exceptional creativity and originality</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 1, 2, 3)">Displays creativity and originality</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 1, 3, 2)">Shows some creativity and originality</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 1, 4, 1)">Lacks significant creativity and originality</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 2, 1, 4)">Innovative use of sprites, backgrounds, and assets</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 2, 2, 3)">Effective use of sprites, backgrounds, and assets</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 2, 3, 2)">Adequate use of sprites, backgrounds, and assets</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 2, 4, 1)">Limited use of sprites, backgrounds, and assets</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 3, 1, 4)">Original storyline, game mechanics, or interactive elements</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 3, 2, 3)">Engaging storyline, game mechanics, or interactive elements</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 3, 3, 2)">A reasonable storyline, game mechanics, or interactive elements</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 3, 4, 1)">Repetitive or unremarkable storyline, game mechanics, or interactive elements</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 4, 1, 4)">Shows a unique and creative approach to the task</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 4, 2, 3)">Demonstrates an imaginative approach to the task</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 4, 3, 2)">Demonstrates a basic level of creativity</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 4, 4, 1)">Lacks a creative approach to the task</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 5, 1, 4)">Clearly surpasses expectations</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 5, 2, 3)">Meets expectations</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 5, 3, 2)">Meets the minimum requirements</button>
                    <button onclick="recordScore(this, 'Creativity and Originality', 5, 4, 1)">Falls below expectations</button>
                </div>
            </div>
        </div>
        <!-- Functionality -->
        <div class="section" style="background-color: lightgreen;">
            <h2>Functionality</h2>
            <div class="rating-table">
                <div class="rating-buttons">
                    <!-- Rating buttons -->
                    <button onclick="recordScore(this, 'Functionality', 1, 1, 4)">Project functions flawlessly without any errors or glitches</button>
                    <button onclick="recordScore(this, 'Functionality', 1, 2, 3)">Project functions well with minor issues</button>
                    <button onclick="recordScore(this, 'Functionality', 1, 3, 2)">Project functions with noticeable errors</button>
                    <button onclick="recordScore(this, 'Functionality', 1, 4, 1)">Project functions with significant errors</button>
                    <button onclick="recordScore(this, 'Functionality', 2, 1, 4)">All features, sprites, and scripts work as intended</button>
                    <button onclick="recordScore(this, 'Functionality', 2, 2, 3)">Most features, sprites, and scripts work as intended</button>
                    <button onclick="recordScore(this, 'Functionality', 2, 3, 2)">Some features, sprites, and scripts may not work as intended</button>
                    <button onclick="recordScore(this, 'Functionality', 2, 4, 1)">Many features, sprites, or scripts do not work as intended</button>
		    <button onclick="recordScore(this, 'Functionality', 3, 1, 4)">No apparent issues with interactivity or navigation</button>
                    <button onclick="recordScore(this, 'Functionality', 3, 2, 3)">Minimal issues with interactivity or navigation</button>
                    <button onclick="recordScore(this, 'Functionality', 3, 3, 2)">Occasional issues with interactivity or navigation</button>
                    <button onclick="recordScore(this, 'Functionality', 3, 4, 1)">Frequent issues with interactivity or navigation</button>          
		    <button onclick="recordScore(this, 'Functionality', 4, 1, 4)">All events and triggers are well-coordinated</button>
                    <button onclick="recordScore(this, 'Functionality', 4, 2, 3)">Most events and triggers are well-coordinated</button>
                    <button onclick="recordScore(this, 'Functionality', 4, 3, 2)">Some events and triggers require improvement</button>
                    <button onclick="recordScore(this, 'Functionality', 4, 4, 1)">Poor coordination of events and triggers</button>
		    <button onclick="recordScore(this, 'Functionality', 5, 1, 4)">Exceptionally well-executed</button>
                    <button onclick="recordScore(this, 'Functionality', 5, 2, 3)">A solid and functional execution</button>
                    <button onclick="recordScore(this, 'Functionality', 5, 3, 2)">A basic level of functionality</button>
                    <button onclick="recordScore(this, 'Functionality', 5, 4, 1)">Subpar functionality</button>
		    <button onclick="recordScore(this, 'Functionality', 6, 1, 4)">Beyond expectations</button>
                    <button onclick="recordScore(this, 'Functionality', 6, 2, 3)">Meets expectations</button>
                    <button onclick="recordScore(this, 'Functionality', 6, 3, 2)">Meets the minimum requirements</button>
                    <button onclick="recordScore(this, 'Functionality', 6, 4, 1)">Falls below expectations</button>
                </div>
            </div>
        </div>
        <!-- Effort and Engagement -->
        <div class="section" style="background-color: lightpink;">
            <h2>Effort and Engagement</h2>
            <div class="rating-table">
                <div class="rating-buttons">
                    <!-- Rating buttons -->
                    <button onclick="recordScore(this, 'Effort and Engagement', 1, 1, 4)">Clearly demonstrates a high level of effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 1, 2, 3)">Demonstrates a good level of effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 1, 3, 2)">Displays some effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 1, 4, 1)">Shows minimal effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 2, 1, 4)">The project is highly engaging, interactive, and immersive</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 2, 2, 3)">The project is engaging and interactive</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 2, 3, 2)">The project is moderately engaging</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 2, 4, 1)">The project lacks engagement and interactivity</button>
		    <button onclick="recordScore(this, 'Effort and Engagement', 3, 1, 4)">Extensive use of Scratch's features and capabilities</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 3, 2, 3)">Effective use of Scratch's features and capabilities</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 3, 3, 2)">Basic use of Scratch's features and capabilities</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 3, 4, 1)">Limited use of Scratch's features and capabilities</button>  
        	    <button onclick="recordScore(this, 'Effort and Engagement', 4, 1, 4)">Evidence of significant time and dedication</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 4, 2, 3)">Evidence of reasonable time and dedication</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 4, 3, 2)">Evidence of limited time and dedication</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 4, 4, 1)">Evidence of little time and dedication</button>
		    <button onclick="recordScore(this, 'Effort and Engagement', 5, 1, 4)">Excels in effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 5, 2, 3)">Good effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 5, 3, 2)">Satisfactory effort and engagement</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 5, 4, 1)">Little effort and engagement</button>
		    <button onclick="recordScore(this, 'Effort and Engagement', 6, 1, 4)">Exceeds expectations</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 6, 2, 3)">Meets expectations</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 6, 3, 2)">Meets the minimum requirements</button>
                    <button onclick="recordScore(this, 'Effort and Engagement', 6, 4, 1)">Falls below expectations</button>
               </div>
            </div>
        </div>
        <!-- Coding Skills -->
        <div class="section" style="background-color: lightyellow;">
            <h2>Coding Skills</h2>
            <div class="rating-table">
                <div class="rating-buttons">
                    <!-- Rating buttons -->
                    <button onclick="recordScore(this, 'Coding Skills', 1, 1, 4)">Exceptional coding skills demonstrated through well-organized scripts</button>
                    <button onclick="recordScore(this, 'Coding Skills', 1, 2, 3)">Strong coding skills demonstrated through organized scripts</button>
                    <button onclick="recordScore(this, 'Coding Skills', 1, 3, 2)">Basic coding skills demonstrated with some organization</button>
                    <button onclick="recordScore(this, 'Coding Skills', 1, 4, 1)">Limited coding skills demonstrated with disorganized scripts</button>
                    <button onclick="recordScore(this, 'Coding Skills', 2, 1, 4)">Effective use of control structures, loops, and variables</button>
                    <button onclick="recordScore(this, 'Coding Skills', 2, 2, 3)">Effective use of control structures, loops, and variables</button>
                    <button onclick="recordScore(this, 'Coding Skills', 2, 3, 2)">Adequate use of control structures, loops, and variables</button>
                    <button onclick="recordScore(this, 'Coding Skills', 2, 4, 1)">Minimal use of control structures, loops, and variables</button>
                    <button onclick="recordScore(this, 'Coding Skills', 3, 1, 4)">Advanced coding techniques employed</button>
                    <button onclick="recordScore(this, 'Coding Skills', 3, 2, 3)">Solid coding techniques employed</button>
                    <button onclick="recordScore(this, 'Coding Skills', 3, 3, 2)">Basic coding techniques employed</button>
                    <button onclick="recordScore(this, 'Coding Skills', 3, 4, 1)">Coding techniques are rudimentary</button>
                    <button onclick="recordScore(this, 'Coding Skills', 4, 1, 4)">Code is clean, well-commented, and easy to understand</button>
                    <button onclick="recordScore(this, 'Coding Skills', 4, 2, 3)">Code is well-commented and mostly clear</button>
                    <button onclick="recordScore(this, 'Coding Skills', 4, 3, 2)">Code may lack clarity and sufficient commenting</button>
                    <button onclick="recordScore(this, 'Coding Skills', 4, 4, 1)">Code lacks clarity and sufficient commenting</button>
                    <button onclick="recordScore(this, 'Coding Skills', 5, 1, 4)">Code exceeds expectations</button>
                    <button onclick="recordScore(this, 'Coding Skills', 5, 2, 3)">Code meets expectations</button>
                    <button onclick="recordScore(this, 'Coding Skills', 5, 3, 2)">Code meets the minimum requirements</button>
                    <button onclick="recordScore(this, 'Coding Skills', 5, 4, 1)">Falls below expectations</button>
                </div>
            </div>
        </div>
        <!-- Documentation and Comments -->
        <div class="section" style="background-color: lightcoral;">
            <h2>Documentation and Comments</h2>
            <div class="rating-table">
                <div class="rating-buttons">
                    <!-- Rating buttons -->
                    <button onclick="recordScore(this, 'Documentation and Comments', 1, 1, 4)">Exceptional documentation with detailed comments</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 1, 2, 3)">Good documentation with comments</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 1, 3, 2)">Basic documentation with minimal comments</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 1, 4, 1)">Limited documentation with few comments</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 2, 1, 4)">Comprehensive explanations of code structure and functionality</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 2, 2, 3)">Adequate explanations of code structure and functionality</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 2, 3, 2)">Limited explanations of code structure and functionality</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 2, 4, 1)">Minimal explanations of code structure and functionality</button>
		    <button onclick="recordScore(this, 'Documentation and Comments', 3, 1, 4)">Comments contribute significantly to code clarity</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 3, 2, 3)">Comments enhance code clarity to some extent</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 3, 3, 2)">Comments provide minimal code clarity</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 3, 4, 1)">Comments do not contribute to code clarity</button>
		    <button onclick="recordScore(this, 'Documentation and Comments', 4, 1, 4)">Clearly exceeds expectations</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 4, 2, 3)">Meets expectations</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 4, 3, 2)">Meets the minimum requirements</button>
                    <button onclick="recordScore(this, 'Documentation and Comments', 4, 4, 1)">Falls below expectations</button>
                </div>
            </div>
        </div>
        
        <button id="printButton" onclick="printScreen()">Print</button>
    </div>
        <script>
    // Data structure to store selected buttons
    const selectedButtons = {};

    // Data structure to store scores for each row
    const rowScores = {
        'Creativity and Originality': [],
        'Functionality': [],
        'Effort and Engagement': [],
        'Coding Skills': [],
        'Documentation and Comments': []
    };

    // Function to record a score
    function recordScore(button, section, row, score) {
        // Unselect the previously selected button in the same row
        if (selectedButtons[section] && selectedButtons[section][row]) {
            selectedButtons[section][row].classList.remove('active');
        }

        // Select the clicked button
        button.classList.add('active');

        // Store the selected button
        selectedButtons[section] = selectedButtons[section] || {};
        selectedButtons[section][row] = button;

        // Calculate the recorded score as 5 minus the provided score
        const recordedScore = 5 - score;

        // Update the row score
        rowScores[section][row] = recordedScore;

        // Update the total mark
        updateTotalMark();
    }

    // Function to calculate the total mark
    function updateTotalMark() {
        let totalMark = 0;

        // Calculate the total mark based on row scores
        for (const section in rowScores) {
            const rowScore = rowScores[section].reduce((sum, score) => sum + score, 0);
            totalMark += rowScore;
        }

        // Update the total mark displayed on the page
        document.getElementById('total-mark').textContent = Math.round((totalMark/104)*100) +"%";
    }

    // JavaScript code to handle the button click event
    document.getElementById("printButton").addEventListener("click", function() {
        window.print(); // This will trigger the print dialog
    });
    
    
    
    
    
   // Get references to the buttons and input elements
    const insertButtons = document.querySelectorAll(".insert-button");
    const studentInputs = document.querySelectorAll(".student-input.student-hidden");

    // Add click event listeners to the "Insert New Student" buttons
    insertButtons.forEach((button) => {
        button.addEventListener("click", () => {
            // Determine the index of the button clicked (2, 3, or 4)
            const columnIndex = parseInt(button.getAttribute("data-index"));

            // Show the corresponding input element
            if (columnIndex >= 2 && columnIndex <= 4) {
                studentInputs[columnIndex - 2].classList.remove("student-hidden");

                // Remove the button
                button.style.display = "none";

                // Create a new header element
                const newHeader = document.createElement("th");
                newHeader.textContent = `Student ${columnIndex}`;

                // Add the new header to the table header row before the input cell
                const table = document.querySelector(".student-table");
                const headerRow = table.rows[0];
                const headerCell = document.createElement("th");
                headerCell.appendChild(newHeader);
                headerRow.insertBefore(headerCell, headerRow.cells[columnIndex - 1]);
            }
        });
    });
    
    

 
        // JavaScript code to make the "Total Mark" section fixed when scrolling
        window.addEventListener("scroll", function() {
            const totalMarkSection = document.getElementById("fixedTotalMark");
            if (window.scrollY > 0) {
                totalMarkSection.style.transform = "translateY(0)";
            } else {
                totalMarkSection.style.transform = "translateY(-100%)";
            }
        });




    
    
</script>



</body>
</html>
