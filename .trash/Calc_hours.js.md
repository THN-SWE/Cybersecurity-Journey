module.exports = {
    Calc_hours: (start, end) => {
        const [sh, sm] = start.split(":").map(Number);
        const [eh, em] = end.split(":").map(Number);
        const diff = (eh * 60 + em - (sh * 60 + sm)) / 60;
        return diff.toFixed(2);
    },
    calc_day_total: (hoursArray) => {
        const total = hoursArray.reduce((a, b) => a + parseFloat(b), 0);
        return total.toFixed(2);
    }
};