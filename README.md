export default function DailyExpenseTracker() {
  return (
    <div className="min-h-screen bg-gray-100 p-6 flex items-center justify-center">
      <div className="bg-white shadow-xl rounded-3xl p-8 w-full max-w-3xl">
        <h1 className="text-3xl font-bold mb-2 text-center">Daily Expense Tracker</h1>
        <p className="text-gray-500 text-center mb-6">
          Record your expenses every day.
        </p>

        <div className="overflow-x-auto">
          <table className="w-full border border-gray-200 rounded-xl overflow-hidden">
            <thead className="bg-gray-200">
              <tr>
                <th className="p-3 text-left">Date</th>
                <th className="p-3 text-left">Category</th>
                <th className="p-3 text-left">Description</th>
                <th className="p-3 text-left">Amount</th>
              </tr>
            </thead>
            <tbody>
              {Array.from({ length: 10 }).map((_, index) => (
                <tr key={index} className="border-t border-gray-200">
                  <td className="p-3">
                    <input
                      type="date"
                      className="w-full border rounded-lg p-2"
                    />
                  </td>
                  <td className="p-3">
                    <select className="w-full border rounded-lg p-2">
                      <option>Food</option>
                      <option>Transportation</option>
                      <option>School</option>
                      <option>Bills</option>
                      <option>Others</option>
                    </select>
                  </td>
                  <td className="p-3">
                    <input
                      type="text"
                      placeholder="Enter details"
                      className="w-full border rounded-lg p-2"
                    />
                  </td>
                  <td className="p-3">
                    <input
                      type="number"
                      placeholder="0.00"
                      className="w-full border rounded-lg p-2"
                    />
                  </td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>

        <div className="mt-6 bg-gray-50 p-4 rounded-2xl border border-gray-200">
          <h2 className="text-xl font-semibold mb-2">Tips</h2>
          <ul className="list-disc list-inside text-gray-600 space-y-1">
            <li>Update your expenses daily.</li>
            <li>Separate wants and needs.</li>
            <li>Review your spending every week.</li>
          </ul>
        </div>
      </div>
    </div>
  );
}
