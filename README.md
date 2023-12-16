# Cooking club membership enrollment system
 Login C# code
private void btnLogin_Click(object sender, EventArgs e)
{
    string username = txtUsername.Text;
    string password = txtPassword.Text;

    if (username == "Admin" && password == "Skills@123")
    {
        RegistrationForm registrationForm = new RegistrationForm();
        registrationForm.Show();
        this.Hide();
    }
    else
    {
        MessageBox.Show("Invalid username or password. Please try again.", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);
    }
}

private void btnClear_Click(object sender, EventArgs e)
{
    txtUsername.Text = "";
    txtPassword.Text = "";
    txtUsername.Focus();
}

private void btnExit_Click(object sender, EventArgs e)
{
    DialogResult result = MessageBox.Show("Are you sure you want to exit?", "Exit", MessageBoxButtons.YesNo, MessageBoxIcon.Question);
    if (result == DialogResult.Yes)
    {
        Application.Exit();
    }
}