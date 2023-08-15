// Loop through each character and use JavaScript to simulate keypress
            foreach (char c in textToEnter)
            {
                ((IJavaScriptExecutor)driver).ExecuteScript(
                    $"arguments[0].dispatchEvent(new KeyboardEvent('keypress', {{ key: '{c}', charCode: '{(int)c}', keyCode: '{(int)c}' }}));", 
                    inputElement);
                Thread.Sleep(100); // Add a small delay between characters (optional)
            }
