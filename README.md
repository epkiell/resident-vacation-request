# resident-vacation-request
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Resident Vacation Request</title>

    <style>

        * {

            margin: 0;

            padding: 0;

            box-sizing: border-box;

        }

        

        body {

            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;

            background: linear-gradient(to bottom right, #fef3c7, #fbbf24);

            min-height: 100vh;

            padding: 1rem;

        }

        

        .container {

            max-width: 42rem;

            margin: 2rem auto;

        }

        

        .card {

            background: white;

            border-radius: 0.5rem;

            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);

            padding: 1.5rem;

        }

        

        .header {

            display: flex;

            align-items: center;

            gap: 0.75rem;

            margin-bottom: 1.5rem;

        }

        

        h1 {

            font-size: 1.5rem;

            font-weight: bold;

            color: #1f2937;

        }

        

        .form-group {

            margin-bottom: 1rem;

        }

        

        label {

            display: block;

            font-size: 0.875rem;

            font-weight: 500;

            color: #374151;

            margin-bottom: 0.25rem;

        }

        

        input[type="text"], input[type="date"] {

            width: 100%;

            padding: 0.5rem 1rem;

            border: 1px solid #d1d5db;

            border-radius: 0.5rem;

            font-size: 1rem;

            font-family: inherit;

        }

        

        input:focus {

            outline: none;

            border-color: #ca8a04;

            box-shadow: 0 0 0 3px rgba(202, 138, 4, 0.1);

        }

        

        .date-grid {

            display: grid;

            grid-template-columns: 1fr 1fr;

            gap: 0.75rem;

        }

        

        .radio-group, .checkbox-group {

            display: flex;

            flex-direction: column;

            gap: 0.5rem;

        }

        

        .radio-label, .checkbox-label {

            display: flex;

            align-items: center;

            cursor: pointer;

        }

        

        input[type="radio"], input[type="checkbox"] {

            width: 1rem;

            height: 1rem;

            margin-right: 0.5rem;

            cursor: pointer;

        }

        

        input[type="radio"] {

            accent-color: #ca8a04;

        }

        

        input[type="checkbox"] {

            accent-color: #ca8a04;

            border-radius: 0.25rem;

        }

        

        .coverage-section {

            background: #f9fafb;

            padding: 1rem;

            border-radius: 0.5rem;

        }

        

        .hidden {

            display: none;

        }

        

        .detail-input {

            margin-top: 0.75rem;

        }

        

        button.submit-btn {

            width: 100%;

            background: #000;

            color: white;

            padding: 0.75rem 1.5rem;

            border: none;

            border-radius: 0.5rem;

            font-size: 1rem;

            font-weight: 500;

            cursor: pointer;

            transition: background 0.2s;

            display: flex;

            align-items: center;

            justify-content: center;

            gap: 0.5rem;

        }

        

        button.submit-btn:hover {

            background: #1f2937;

        }

        

        button.submit-btn:disabled {

            background: #d1d5db;

            cursor: not-allowed;

        }

        

        .success {

            text-align: center;

            padding: 3rem 0;

        }

        

        .success-icon {

            width: 4rem;

            height: 4rem;

            margin: 0 auto 1rem;

            color: #10b981;

        }

        

        .success h2 {

            font-size: 1.25rem;

            font-weight: 600;

            color: #1f2937;

            margin-bottom: 0.5rem;

        }

        

        .success p {

            color: #6b7280;

        }

        

        .footer {

            text-align: center;

            font-size: 0.875rem;

            color: #6b7280;

            margin-top: 1rem;

            opacity: 0.6;

        }

    </style>

</head>

<body>

    <div class="container">

        <div class="card">

            <div class="header">

                <svg width="32" height="32" fill="none" stroke="#ca8a04" viewBox="0 0 24 24">

                    <rect x="3" y="4" width="18" height="18" rx="2" ry="2" stroke-width="2"></rect>

                    <line x1="16" y1="2" x2="16" y2="6" stroke-width="2"></line>

                    <line x1="8" y1="2" x2="8" y2="6" stroke-width="2"></line>

                    <line x1="3" y1="10" x2="21" y2="10" stroke-width="2"></line>

                </svg>

                <h1>Vacation Request</h1>

            </div>

            

            <div id="formView">

                <div class="form-group">

                    <label>Resident Name *</label>

                    <input type="text" id="name" placeholder="Your name">

                </div>

                

                <div class="date-grid">

                    <div class="form-group">

                        <label>Start Date *</label>

                        <input type="date" id="startDate">

                    </div>

                    <div class="form-group">

                        <label>End Date *</label>

                        <input type="date" id="endDate">

                    </div>

                </div>

                

                <div class="form-group">

                    <label>Type of Leave *</label>

                    <div class="radio-group">

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Vacation">

                            <span>Vacation</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Flex Day">

                            <span>Flex Day</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Professional Day">

                            <span>Professional Day</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Bereavement">

                            <span>Bereavement</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Sick Day">

                            <span>Sick Day</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Course - specify below">

                            <span>Course - specify below</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Conference Attendance - specify below">

                            <span>Conference Attendance - specify below</span>

                        </label>

                        <label class="radio-label">

                            <input type="radio" name="leaveType" value="Medical Leave">

                            <span>Medical Leave</span>

                        </label>

                    </div>

                    

                    <div id="courseDetails" class="detail-input hidden">

                        <input type="text" id="courseDetailsInput" placeholder="Specify course name or details">

                    </div>

                    

                    <div id="conferenceDetails" class="detail-input hidden">

                        <input type="text" id="conferenceDetailsInput" placeholder="Specify conference name or details">

                    </div>

                </div>

                

                <div class="form-group coverage-section">

                    <label>Coverage Addressed (check all that apply)</label>

                    <div class="checkbox-group" style="margin-top: 0.75rem;">

                        <label class="checkbox-label">

                            <input type="checkbox" id="traumaClinic">

                            <span>Trauma Clinic</span>

                        </label>

                        <label class="checkbox-label">

                            <input type="checkbox" id="opdClinic">

                            <span>OPD Clinic</span>

                        </label>

                        <label class="checkbox-label">

                            <input type="checkbox" id="call">

                            <span>Call</span>

                        </label>

                        <label class="checkbox-label">

                            <input type="checkbox" id="pedsOpdClinic">

                            <span>Peds OPD Clinic</span>

                        </label>

                    </div>

                </div>

                

                <button class="submit-btn" id="submitBtn" disabled>

                    <svg width="20" height="20" fill="none" stroke="currentColor" viewBox="0 0 24 24">

                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>

                    </svg>

                    Submit Request

                </button>

            </div>

            

            <div id="successView" class="success hidden">

                <svg class="success-icon" fill="none" stroke="currentColor" viewBox="0 0 24 24">

                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>

                </svg>

                <h2>Request Submitted!</h2>

                <p>Your email client should open with the vacation request.</p>

            </div>

        </div>

        

        <p class="footer">Built by Brian Downs</p>

    </div>



    <script>

        // Set minimum date to today

        const today = new Date().toISOString().split('T')[0];

        document.getElementById('startDate').setAttribute('min', today);

        document.getElementById('endDate').setAttribute('min', today);

        

        // Get form elements

        const nameInput = document.getElementById('name');

        const startDateInput = document.getElementById('startDate');

        const endDateInput = document.getElementById('endDate');

        const leaveTypeRadios = document.querySelectorAll('input[name="leaveType"]');

        const courseDetailsDiv = document.getElementById('courseDetails');

        const courseDetailsInput = document.getElementById('courseDetailsInput');

        const conferenceDetailsDiv = document.getElementById('conferenceDetails');

        const conferenceDetailsInput = document.getElementById('conferenceDetailsInput');

        const traumaClinicCheck = document.getElementById('traumaClinic');

        const opdClinicCheck = document.getElementById('opdClinic');

        const callCheck = document.getElementById('call');

        const pedsOpdClinicCheck = document.getElementById('pedsOpdClinic');

        const submitBtn = document.getElementById('submitBtn');

        const formView = document.getElementById('formView');

        const successView = document.getElementById('successView');

        

        let selectedLeaveType = '';

        

        // Handle leave type selection

        leaveTypeRadios.forEach(radio => {

            radio.addEventListener('change', function() {

                selectedLeaveType = this.value;

                

                // Show/hide detail inputs

                if (selectedLeaveType === 'Course - specify below') {

                    courseDetailsDiv.classList.remove('hidden');

                    conferenceDetailsDiv.classList.add('hidden');

                } else if (selectedLeaveType === 'Conference Attendance - specify below') {

                    conferenceDetailsDiv.classList.remove('hidden');

                    courseDetailsDiv.classList.add('hidden');

                } else {

                    courseDetailsDiv.classList.add('hidden');

                    conferenceDetailsDiv.classList.add('hidden');

                }

                

                validateForm();

            });

        });

        

        // Update end date minimum when start date changes

        startDateInput.addEventListener('change', function() {

            endDateInput.setAttribute('min', this.value);

            validateForm();

        });

        

        // Validate form

        function validateForm() {

            const isValid = nameInput.value && 

                          startDateInput.value && 

                          endDateInput.value && 

                          selectedLeaveType;

            submitBtn.disabled = !isValid;

        }

        

        // Add event listeners

        [nameInput, startDateInput, endDateInput].forEach(input => {

            input.addEventListener('input', validateForm);

        });

        

        // Handle submit

        submitBtn.addEventListener('click', function() {

            // Build coverage list

            const coverageItems = [];

            if (traumaClinicCheck.checked) coverageItems.push('Trauma Clinic');

            if (opdClinicCheck.checked) coverageItems.push('OPD Clinic');

            if (callCheck.checked) coverageItems.push('Call');

            if (pedsOpdClinicCheck.checked) coverageItems.push('Peds OPD Clinic');

            

            const coverageStatus = coverageItems.length > 0 

                ? coverageItems.join(', ') 

                : 'None indicated';

            

            // Build details section

            let detailsSection = '';

            if (selectedLeaveType === 'Course - specify below' && courseDetailsInput.value) {

                detailsSection = `\nCourse Details: ${courseDetailsInput.value}`;

            } else if (selectedLeaveType === 'Conference Attendance - specify below' && conferenceDetailsInput.value) {

                detailsSection = `\nConference Details: ${conferenceDetailsInput.value}`;

            }

            

            const subject = encodeURIComponent(`Vacation Request - ${nameInput.value} - ${startDateInput.value} to ${endDateInput.value}`);

            const body = encodeURIComponent(`RESIDENT VACATION REQUEST



Resident Name: ${nameInput.value}

Leave Type: ${selectedLeaveType}${detailsSection}



DATES:

Start Date: ${startDateInput.value}

End Date: ${endDateInput.value}



COVERAGE ADDRESSED FOR:

${coverageStatus}



---

Please reply to this email with "Approved" or "Denied" along with any comments.



This request was submitted via the Resident Vacation Request system.`);

            

            window.location.href = `mailto:Jakisha.Shepherd@advocatehealth.org?subject=${subject}&body=${body}`;

            

            // Show success

            formView.classList.add('hidden');

            successView.classList.remove('hidden');

            

            // Reset after 3 seconds

            setTimeout(function() {

                nameInput.value = '';

                startDateInput.value = '';

                endDateInput.value = '';

                leaveTypeRadios.forEach(r => r.checked = false);

                selectedLeaveType = '';

                courseDetailsInput.value = '';

                conferenceDetailsInput.value = '';

                courseDetailsDiv.classList.add('hidden');

                conferenceDetailsDiv.classList.add('hidden');

                traumaClinicCheck.checked = false;

                opdClinicCheck.checked = false;

                callCheck.checked = false;

                pedsOpdClinicCheck.checked = false;

                formView.classList.remove('hidden');

                successView.classList.add('hidden');

                validateForm();

            }, 3000);

        });

    </script>

</body>

</html>
