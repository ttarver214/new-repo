<form id="MT_DATA_FORM" action="your_action_url" method="post">
    <input type="email" id="email" name="email" placeholder="Enter your email">
    <button type="submit">Submit</button>
</form>

<script>
    document.getElementById('MT_DATA_FORM').addEventListener('submit', function(event) {
        var blockedDomains = ['domain1.com', 'domain2.com']; // Add the domains you want to block here
        var emailInput = document.getElementById('email').value;
        var domain = emailInput.split('@')[1]; // Get the domain part of the email

        if (blockedDomains.includes(domain)) {
            alert('Sorry, emails from this domain are not allowed.');
            event.preventDefault(); // Prevent form submission
        }
    });
</script>
