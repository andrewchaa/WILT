### date

    const today = new Date()                      // today's date

    const yearAgo = new Date()
    yearAgo.setFullYear(today.getFullYear() - 1)  // a year ago
    
    today.toString('YYYY-MM-DD')                  // format date string

### string

    csv += `${date.toDateString()},${low},${high},${open},${close},${volumn}\r\n`  // templating
