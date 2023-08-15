 Actions actions = new Actions(driver);

            // Click on the input field to focus on it
            actions.Click(inputElement).Build().Perform();

            // Loop through each character and send it using SendKeys
            foreach (char c in textToEnter)
            {
                actions.SendKeys(c.ToString()).Build().Perform();
                Thread.Sleep(100); // Add a small delay between characters (optional)
            }
